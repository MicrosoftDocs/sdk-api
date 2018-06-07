---
UID: TP:audio
ms.assetid: 91b97f1d-92f1-3c32-955a-dd6524d5b764
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Audio Devices DDI Reference



Overview of the Audio Devices DDI Reference technology.

To develop Audio Devices DDI Reference, you need these headers:

 * [audiomediatype.h](..\audiomediatype\index.md)
 * [baseaudioprocessingobject.h](..\baseaudioprocessingobject\index.md)
 * [dmusics.h](..\dmusics\index.md)
 * [msapofxproxy.h](..\msapofxproxy\index.md)

For the programming guide, see [Audio Devices DDI Reference](/windows/desktop/audio).

## Functions

| Title   | Description   |
| ---- |:---- |
| [AERT_Allocate function](..\baseaudioprocessingobject\nf-baseaudioprocessingobject-aert_allocate.md) | The AERT_Allocate utility function allocates and locks a segment of memory for use by audio processing objects. |
| [AERT_Free function](..\baseaudioprocessingobject\nf-baseaudioprocessingobject-aert_free.md) | The AERT_Free utility function releases (frees) memory that was locked by the AERT_Allocate function, for use by audio processing objects to process audio data. |
| [CreateAudioMediaType function](..\audiomediatype\nf-audiomediatype-createaudiomediatype.md) | The CreateAudioMediaType function uses the format specified by the caller to create a media type object that describes the audio format. |
| [CreateAudioMediaTypeFromUncompressedAudioFormat function](..\audiomediatype\nf-audiomediatype-createaudiomediatypefromuncompressedaudioformat.md) | The CreateAudioMediaTypeFromUncompressedAudioFormat function uses the information provided in the UNCOMPRESSEDAUDIOFORMAT structure to create a media type object that describes the audio format. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_DMUS_VOICE_STATE structure](..\dmusics\ns-dmusics-_dmus_voice_state.md) | DMUS_VOICE_STATE is not supported and may be altered or unavailable in the future. |
| [_UNCOMPRESSEDAUDIOFORMAT structure](..\audiomediatype\ns-audiomediatype-_uncompressedaudioformat.md) | The UNCOMPRESSEDAUDIOFORMAT structure specifies the frame rate, channel mask, and other attributes of the uncompressed audio data format. |
| [tagKSP_PINMODE structure](..\msapofxproxy\ns-msapofxproxy-tagksp_pinmode.md) | The KSP_PINMODE structure specifies the pin property and the supported audio processing modes for a pin factory. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [KSPROPERTY_AUDIOEFFECTSDISCOVERY enumeration](..\msapofxproxy\ne-msapofxproxy-ksproperty_audioeffectsdiscovery.md) | The KSPROPERTY_AUDIOEFFECTSDISCOVERY enumeration defines a constant that is used by the list of audio processing objects (APOs). |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IAudioMediaType interface](..\audiomediatype\nn-audiomediatype-iaudiomediatype.md) | The IAudioMediaType interface exposes methods that allow an sAPO to get information that is used to negotiate with the audio engine for the appropriate audio data format. |
| [IDirectMusicSynth interface](..\dmusics\nn-dmusics-idirectmusicsynth.md) | The IDirectMusicSynth interface is used by DirectMusic to communicate with user-mode synthesizers. |
| [IDirectMusicSynth8 interface](..\dmusics\nn-dmusics-idirectmusicsynth8.md) | IDirectMusicSynth8 is unsupported and may be altered or unavailable in the future. |
| [IDirectMusicSynthSink interface](..\dmusics\nn-dmusics-idirectmusicsynthsink.md) | The IDirectMusicSynthSink interface is now largely obsolete and is supported only by versions of DirectMusic before DirectX 8. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IAudioMediaType::GetAudioFormat](..\audiomediatype\nf-audiomediatype-iaudiomediatype-getaudioformat.md) | The GetAudioFormat method returns the WAVEFORMATEX structure for the audio data format. |
| [IAudioMediaType::GetUncompressedAudioFormat](..\audiomediatype\nf-audiomediatype-iaudiomediatype-getuncompressedaudioformat.md) | The IAudioMediaType |
| [IAudioMediaType::IsCompressedFormat](..\audiomediatype\nf-audiomediatype-iaudiomediatype-iscompressedformat.md) | The IsCompressedFormat method determines whether the audio data format is a compressed format. |
| [IAudioMediaType::IsEqual](..\audiomediatype\nf-audiomediatype-iaudiomediatype-isequal.md) | The IsEqual method compares two media types and determines whether they are identical. |
| [IDirectMusicSynth8::AssignChannelToBuses](..\dmusics\nf-dmusics-idirectmusicsynth8-assignchanneltobuses.md) | AssignChannelToBuses is unsupported and may be altered or unavailable in the future. |
| [IDirectMusicSynth8::GetVoiceState](..\dmusics\nf-dmusics-idirectmusicsynth8-getvoicestate.md) | GetVoiceState is unsupported and may be altered or unavailable in the future. |
| [IDirectMusicSynth8::PlayVoice](..\dmusics\nf-dmusics-idirectmusicsynth8-playvoice.md) | PlayVoice is unsupported and may be altered or unavailable in the future. |
| [IDirectMusicSynth8::Refresh](..\dmusics\nf-dmusics-idirectmusicsynth8-refresh.md) | Refresh is unsupported and may be altered or unavailable in the future. |
| [IDirectMusicSynth8::StopVoice](..\dmusics\nf-dmusics-idirectmusicsynth8-stopvoice.md) | StopVoice is unsupported and may be altered or unavailable in the future. |
| [IDirectMusicSynth::Activate](..\dmusics\nf-dmusics-idirectmusicsynth-activate.md) | The Activate method enables or disables the audio device under program control. |
| [IDirectMusicSynth::Close](..\dmusics\nf-dmusics-idirectmusicsynth-close.md) | The Close method closes a DirectMusic &#0034;port&#0034;, which is a DirectMusic term for a device that sends or receives music data. |
| [IDirectMusicSynth::Download](..\dmusics\nf-dmusics-idirectmusicsynth-download.md) | The Download method downloads a wave or instrument definition to the synthesizer. |
| [IDirectMusicSynth::GetAppend](..\dmusics\nf-dmusics-idirectmusicsynth-getappend.md) | The GetAppend method outputs the number of additional wave samples that the DirectMusic &#0034;port&#0034; needs to have appended to the end of a download buffer. |
| [IDirectMusicSynth::GetChannelPriority](..\dmusics\nf-dmusics-idirectmusicsynth-getchannelpriority.md) | The GetChannelPriority method outputs the priority of a MIDI channel. |
| [IDirectMusicSynth::GetFormat](..\dmusics\nf-dmusics-idirectmusicsynth-getformat.md) | The GetFormat method retrieves information about the wave format. |
| [IDirectMusicSynth::GetLatencyClock](..\dmusics\nf-dmusics-idirectmusicsynth-getlatencyclock.md) | The GetLatencyClock method retrieves a reference to the IReferenceClock interface (described in the Microsoft Windows SDK documentation) of the reference-clock object that tracks the current mix time. |
| [IDirectMusicSynth::GetPortCaps](..\dmusics\nf-dmusics-idirectmusicsynth-getportcaps.md) | The GetPortCaps method retrieves the capabilities of a DirectMusic &#0034;port&#0034;, which is a DirectMusic term for a device that sends or receives music data. |
| [IDirectMusicSynth::GetRunningStats](..\dmusics\nf-dmusics-idirectmusicsynth-getrunningstats.md) | The GetRunningStats method retrieves current information about the state of the synthesizer so that an application can tell how the synth is performing. |
| [IDirectMusicSynth::Open](..\dmusics\nf-dmusics-idirectmusicsynth-open.md) | The Open method opens a DirectMusic synthesizer &#0034;port&#0034;. |
| [IDirectMusicSynth::PlayBuffer](..\dmusics\nf-dmusics-idirectmusicsynth-playbuffer.md) | The PlayBuffer method downloads a stream of MIDI messages to the synthesizer. |
| [IDirectMusicSynth::Render](..\dmusics\nf-dmusics-idirectmusicsynth-render.md) | The Render method is called by the synth sink to render to a buffer in the audio stream. |
| [IDirectMusicSynth::SetChannelPriority](..\dmusics\nf-dmusics-idirectmusicsynth-setchannelpriority.md) | The SetChannelPriority method sets the priority of a MIDI channel. |
| [IDirectMusicSynth::SetMasterClock](..\dmusics\nf-dmusics-idirectmusicsynth-setmasterclock.md) | The SetMasterClock method provides the synthesizer with a master time source, which the synthesizer requires to synchronize itself with the rest of DirectMusic. |
| [IDirectMusicSynth::SetNumChannelGroups](..\dmusics\nf-dmusics-idirectmusicsynth-setnumchannelgroups.md) | The SetNumChannelGroups method instructs the synthesizer to set its number of channel groups to a new value. |
| [IDirectMusicSynth::SetSynthSink](..\dmusics\nf-dmusics-idirectmusicsynth-setsynthsink.md) | The SetSynthSink method establishes the connection of the synth to the wave sink. |
| [IDirectMusicSynth::Unload](..\dmusics\nf-dmusics-idirectmusicsynth-unload.md) | The Unload method unloads a DLS resource (waveform or articulation data for a MIDI instrument) that was previously downloaded by a call to IDirectMusicSynth |
| [IDirectMusicSynthSink::Activate](..\dmusics\nf-dmusics-idirectmusicsynthsink-activate.md) | The Activate method activates or deactivates the synthesizer sink. |
| [IDirectMusicSynthSink::GetDesiredBufferSize](..\dmusics\nf-dmusics-idirectmusicsynthsink-getdesiredbuffersize.md) | The GetDesiredBufferSize method retrieves the synthesizer's preferred buffer size, expressed in samples. |
| [IDirectMusicSynthSink::GetLatencyClock](..\dmusics\nf-dmusics-idirectmusicsynthsink-getlatencyclock.md) | The GetLatencyClock method retrieves the latency clock, which measures the progress of the output audio stream. |
| [IDirectMusicSynthSink::Init](..\dmusics\nf-dmusics-idirectmusicsynthsink-init.md) | The Init method initializes the synth-sink object. |
| [IDirectMusicSynthSink::RefTimeToSample](..\dmusics\nf-dmusics-idirectmusicsynthsink-reftimetosample.md) | The RefTimeToSample method converts a reference time to a sample time. |
| [IDirectMusicSynthSink::SampleToRefTime](..\dmusics\nf-dmusics-idirectmusicsynthsink-sampletoreftime.md) | The SampleToRefTime method converts a sample time to a reference time. |
| [IDirectMusicSynthSink::SetDirectSound](..\dmusics\nf-dmusics-idirectmusicsynthsink-setdirectsound.md) | The SetDirectSound method connects the synthesizer sink with an existing DirectSound object and a DirectSound buffer. |
| [IDirectMusicSynthSink::SetMasterClock](..\dmusics\nf-dmusics-idirectmusicsynthsink-setmasterclock.md) | The SetMasterClock method provides the synth sink with a master time source, which is required for synchronization with the rest of DirectMusic. |
