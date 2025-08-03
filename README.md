Harold Hong

https://github.com/monkeyoohlala/blog-ai




Setup instructions:
Create a folder for the project and then use laravel new blog-ai --jet
Create Services folder

Add these files to the project:
    app/Http/Controllers/AIController.php
    app/Services/AIService.php
    resources/views/ai_form.blade.php


Add these to the .env file:
    OPENAI_API_KEY=your_openai_key_here
    OPENAI_API_URL=https://api.openai.com/v1
    OPENAI_MODEL=gpt-3.5-turbo


Add this to services.php in the config folder:
    'openai' => [
        'key' => env('OPENAI_API_KEY'),
        'url' => env('OPENAI_API_URL', 'https://api.openai.com/v1'),
        'model' => env('OPENAI_MODEL', 'gpt-3.5-turbo'),
    ],


Add this to web.php:
    use App\Http\Controllers\AIController;

    Route::get('/ai-form', [AIController::class, 'showForm'])->name('ai.form');
    Route::post('/ai-generate', [AIController::class, 'generate'])->name('ai.generate');


Build the AIController
Create the Service Layer
Build the Blade View

Run with php artisan serve





How to Obtain Open AI API Key:

Navigate to:

    https://platform.openai.com/docs/overview



Description of the App:
    Creates a blog entry



Reflection questions:

1. How did the AI output change when you modified the tone or role in your prompt?
    I asked AI to write me a comedic poem and a casual poem. AI was funny for the comedic poem and relaxing for the casual poem.

2. What would you improve about the API integration for a production app?
    Well I had trouble using OpenAI but I managed to fix it. Other than that, I dont think any change is necessary.

3. What’s one thing you learned about Laravel that you hadn’t used before?
    I did not AI integration would be very awesome! It was fun and new to me. Thank you for this opportunity.