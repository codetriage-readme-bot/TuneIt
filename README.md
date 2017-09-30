# TuneIt

[![](https://www.jitpack.io/v/CuriousNikhil/TuneIt.svg)](https://www.jitpack.io/#CuriousNikhil/TuneIt)

TuneIt is an android library that let's you to create awesome PCM (Pulse-Code Modulation 16 bit) tones in your app!
The setup is very easy just follow the following steps:

<h4>step1</h4>
Add the JitPack repository to your build file
<pre>
<code> 
allprojects {
		repositories {
			...
			maven { url 'https://www.jitpack.io' }
		}
	}
  </code>
</pre>
<h4>step2</h4>
 Add the following dependency in your <code>app/build.gradle</code> file
 <pre>
 <code>
 	dependencies {
	        compile 'com.github.CuriousNikhil:TuneIt:1.0'
	}
 </code>
 </pre>
Tadaa!! now you are set to make some noise ,yeah!!


<h4>step3</h4>
Use the following cod snippet to create your own tone
<pre>
<code>
                    TuneIt.getInitialised().create(frequency, duration, volume, new StopToneListener() {
                        @Override
                        public void onTrackStopped() {
			    //tack playing stopped !
                            Toast.makeText(MainActivity.this, "Track stopped!", Toast.LENGTH_SHORT).show();
                        }
                    });
</code>
</pre>
Initialise or assign 
<code>frequency</code> as <code>int</code><br>
<code>duration</code> as <code>int</code><br>
<code>volume</code> as <code>float (ex: 1.0f for max volume)</code><br><br>
Refer to sample <a href="https://github.com/CuriousNikhil/TuneIt/blob/master/app/src/main/java/xyz/mystikolabs/tuneittest/MainActivity.java">app</a><br><br><br>

Yes you are done! Make your own piyano/casio or flute whatever !!<br>
Any forks/suggestions are always welcome! Focusing on integrating this library with AI to generate music on android.

<pre>
MIT License

Copyright (c) 2017 Nikhil Chaudhari

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
</pre>

