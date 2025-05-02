# audio-to-text-GPU-openai
A notebook using the whisper module from OpenAi (https://pypi.org/project/openai-whisper/) via torch to transcribe audio using the GPU and the FP16 Units.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

# How to use it and things to have in mind:
1.- This notebook uses torch to call in this case an Intel GPU via XPU, if you don't have one it can also be used but it'll use the CPU. 


2.-On this line: " model = whisper.load_model("turbo", device=device) " -> you may want to change the model, wich on this case is turbo, to the one that fits your hardware, there are various models that 
can be consulted on the first link here. 


3.- On this line: " result = model.transcribe(file, fp16=True)  " -> the fp16 is enabled, but can only be used and will be used when its True and your Hardware supports it, so i recommend to execute the celds above to know it, if not, you can just set it to False to avoid problems.


# When executing:
1.- The first input ask the name of the file, your input can be comething like: audio.mp3


2.- The second input ask you the name you want for your output file, you can write something like: example.txt

# Enjoy :)
