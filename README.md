# React Audio Player

React Audio Player is a custom player that I created for use on my websites. This component offers seamless audio control on a page by automatically pausing playback on one instance when another is activated. It includes two variations and support for multiple instances per page.

To read more about this player please visit my [website](https://rokasdanevicius.com/ReactAudio).

## Usage

To use the React Audio Player for your own project, follow these steps:

1. Find the `AudioState` component, which checks the states of the players.
2. Choose one of the two player components: `AudioSimple` or `AudioSimpleTimer`.
3. Download the CSS stylesheet for the player component you've chosen.
4. Refer to the code snippet below for instructions on how to implement them.

```jsx
import { AudioProvider } from 'AudioState';
import AudioSimple from 'AudioSimple';
import AudioSimpleTimer from 'AudioSimpleTimer';

const YourPage = () => {
  return (
    <div>
      {/* Audio provider which checks for active players. */}
      {/* You can place other tags inside, this will not affect HTML placement or style. */}
      <AudioProvider>
        {/* Both audio players can be used in the same page. */}
        {/* Make sure to set the id to a different number on each track so the provider can keep track of them. */}
        {/* Audio player without the timer. */}
        <AudioSimple id="1" to='/' link="YourAudio.mp3" description="Your description." />
        {/* Audio player with the timer. */}
        <AudioSimpleTimer id="2" to='/' link="YourAudio.mp3" description="Your description." />
      </AudioProvider>
    </div>
  );
}
