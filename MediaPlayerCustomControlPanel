import React from 'react';
import './style.css'

function CustomVideoPlayerControlPanel(props) {
    return (
        <div className='row d-flex m-0 custom-player-controller'>
            <div className='custom-player-controller-play-pause text-center' >
                {props.playing && <p onClick={props.handlePause} className='m-0'><i className="fa fa-pause text-white" /></p>}
                {!props.playing && <p onClick={props.handlePlay} className='m-0'><i className="fa fa-play text-white" /></p>}
            </div>
            <div className='custom-player-controller-volumne row m-0 ' style={{
                alignItems: 'center'
            }}>
                <div style={{ alignSelf: 'center', margin: '0px 5px', width: '10%' }}>
                    {props.volume > 50 && <i className='fa fa-volume-up text-white' />}
                    {
                        // eslint-disable-next-line
                        props.volume == 0 && <i className='fa fa-volume-mute text-white' />}
                    {props.volume <= 50 && props.volume > 0 && <i className='fa fa-volume-down text-white' />}
                </div>
                <input
                    className='volum-range'
                    style={{ width: "80%" }}
                    type="range"
                    min={0} max={100}
                    value={props.volume}
                    onInput={(e) => props.handleVolumeChange(e)} />
            </div>
            <div className='custom-player-controller-video-progress row m-0 justify-content-center align-self-center'>
                <input
                    className='seek-range'
                    style={{ width: "90%" }}
                    type="range"
                    min={0}
                    max={props.totalDurationOfVideo}
                    onInput={(e) => props.handleSeekChange(e)}
                    value={props.currentSeek} />
            </div>
        </div>
    );
}

export default CustomVideoPlayerControlPanel;
