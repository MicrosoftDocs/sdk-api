---
UID: TP:xaudio2
ms.assetid: f4dc61e6-fea4-3675-94bd-c29e3ea2b7f0
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# XAudio2 APIs

## -description

Overview of the XAudio2 APIs technology.

To develop XAudio2 APIs, you need these headers:

 * [hrtfapoapi.h](..\hrtfapoapi\index.md)
 * [x3daudio.h](..\x3daudio\index.md)
 * [xapo.h](..\xapo\index.md)
 * [xapobase.h](..\xapobase\index.md)
 * [xapofx.h](..\xapofx\index.md)
 * [xaudio2.h](..\xaudio2\index.md)
 * [xaudio2fx.h](..\xaudio2fx\index.md)

For the programming guide, see [XAudio2 APIs](/windows/desktop/xaudio2).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CreateFX function](..\xapofx\nf-xapofx-createfx.md) | Creates an instance of the requested XAPOFX effect. |
| [CreateHrtfApo function](..\hrtfapoapi\nf-hrtfapoapi-createhrtfapo.md) | Creates an instance of the IXAPO interface for head-related transfer function (HRTF) processing. |
| [ReverbConvertI3DL2ToNative function](..\xaudio2fx\nf-xaudio2fx-reverbconverti3dl2tonative.md) | Inline function that converts I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters to native XAudio2 parameters. |
| [X3DAudioCalculate function](..\x3daudio\nf-x3daudio-x3daudiocalculate.md) | Calculates DSP settings with respect to 3D parameters. |
| [X3DAudioInitialize function](..\x3daudio\nf-x3daudio-x3daudioinitialize.md) | Sets all global 3D audio constants. |
| [XAudio2AmplitudeRatioToDecibels function](..\xaudio2\nf-xaudio2-xaudio2amplituderatiotodecibels.md) | Inline function that converts an amplitude ratio value to a decibel value. |
| [XAudio2Create function](..\xaudio2\nf-xaudio2-xaudio2create.md) | Creates a new XAudio2 object and returns a pointer to its IXAudio2 interface. |
| [XAudio2CreateReverb function](..\xaudio2fx\nf-xaudio2fx-xaudio2createreverb.md) | Creates a new reverb audio processing object (APO), and returns a pointer to it. |
| [XAudio2CreateVolumeMeter function](..\xaudio2fx\nf-xaudio2fx-xaudio2createvolumemeter.md) | Creates a new volume meter audio processing object (APO) and returns a pointer to it. |
| [XAudio2CutoffFrequencyToOnePoleCoefficient function](..\xaudio2\nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient.md) | Inline function that converts from filter cutoff frequencies expressed in hertz to the filter coefficients used with the Frequency member of the XAUDIO2_FILTER_PARAMETERS structure. |
| [XAudio2CutoffFrequencyToRadians function](..\xaudio2\nf-xaudio2-xaudio2cutofffrequencytoradians.md) | Inline function that converts from filter cutoff frequencies expressed in hertz to the radian frequency values used in the Frequency member of the XAUDIO2_FILTER_PARAMETERS structure. |
| [XAudio2DecibelsToAmplitudeRatio function](..\xaudio2\nf-xaudio2-xaudio2decibelstoamplituderatio.md) | Inline function that converts a decibel value to an amplitude ratio value. |
| [XAudio2FrequencyRatioToSemitones function](..\xaudio2\nf-xaudio2-xaudio2frequencyratiotosemitones.md) | Inline function that converts a frequency ratio value to a semitone value. |
| [XAudio2RadiansToCutoffFrequency function](..\xaudio2\nf-xaudio2-xaudio2radianstocutofffrequency.md) | Inline function that converts from the radian frequencies used in XAUDIO2_FILTER_PARAMETERS back to absolute frequencies in hertz. |
| [XAudio2SemitonesToFrequencyRatio function](..\xaudio2\nf-xaudio2-xaudio2semitonestofrequencyratio.md) | Inline function that converts a semitone value to a frequency ratio value. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [FXECHO_INITDATA structure](..\xapofx\ns-xapofx-fxecho_initdata.md) | Initialization parameters for use with the FXECHO XAPOFX. |
| [FXECHO_PARAMETERS structure](..\xapofx\ns-xapofx-fxecho_parameters.md) | Parameters for use with the FXECHO XAPOFX. |
| [FXEQ_PARAMETERS structure](..\xapofx\ns-xapofx-fxeq_parameters.md) | Parameters for use with the FXEQ XAPO. |
| [FXMASTERINGLIMITER_PARAMETERS structure](..\xapofx\ns-xapofx-fxmasteringlimiter_parameters.md) | Parameters for use with the FXMasteringLimiter XAPO. |
| [FXREVERB_PARAMETERS structure](..\xapofx\ns-xapofx-fxreverb_parameters.md) | Parameters for use with the FXReverb XAPO. |
| [HrtfApoInit structure](..\hrtfapoapi\ns-hrtfapoapi-hrtfapoinit.md) | Specifies parameters used to initialize HRTF spatial audio. |
| [HrtfDirectivity structure](..\hrtfapoapi\ns-hrtfapoapi-hrtfdirectivity.md) | Base directivity pattern descriptor. Describes the type of directivity applied to a sound. |
| [HrtfDirectivityCardioid structure](..\hrtfapoapi\ns-hrtfapoapi-hrtfdirectivitycardioid.md) | Describes a cardioid directivity pattern. |
| [HrtfDirectivityCone structure](..\hrtfapoapi\ns-hrtfapoapi-hrtfdirectivitycone.md) | Describes a cone directivity. |
| [HrtfDistanceDecay structure](..\hrtfapoapi\ns-hrtfapoapi-hrtfdistancedecay.md) | Describes a distance-based decay behavior. |
| [HrtfOrientation structure](..\hrtfapoapi\ns-hrtfapoapi-hrtforientation.md) | Indicates the orientation of an HRTF directivity object. |
| [HrtfPosition structure](..\hrtfapoapi\ns-hrtfapoapi-hrtfposition.md) | Represents a position in 3D space, using a right-handed coordinate system. |
| [X3DAUDIO_CONE structure](..\x3daudio\ns-x3daudio-x3daudio_cone.md) | Specifies directionality for a single-channel non-LFE emitter by scaling DSP behavior with respect to the emitter's orientation. |
| [X3DAUDIO_DISTANCE_CURVE structure](..\x3daudio\ns-x3daudio-x3daudio_distance_curve.md) | Defines an explicit piecewise curve made up of linear segments, directly defining DSP behavior with respect to normalized distance. |
| [X3DAUDIO_DISTANCE_CURVE_POINT structure](..\x3daudio\ns-x3daudio-x3daudio_distance_curve_point.md) | Defines a DSP setting at a given normalized distance. |
| [X3DAUDIO_DSP_SETTINGS structure](..\x3daudio\ns-x3daudio-x3daudio_dsp_settings.md) | Receives the results from a call to X3DAudioCalculate. |
| [X3DAUDIO_EMITTER structure](..\x3daudio\ns-x3daudio-x3daudio_emitter.md) | Defines a single-point or multiple-point 3D audio source that is used with an arbitrary number of sound channels. |
| [X3DAUDIO_LISTENER structure](..\x3daudio\ns-x3daudio-x3daudio_listener.md) | Defines a point of 3D audio reception. |
| [XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS structure](..\xapo\ns-xapo-xapo_lockforprocess_buffer_parameters.md) | Defines stream buffer parameters that remain constant while an XAPO is locked. Used with the IXAPO |
| [XAPO_PROCESS_BUFFER_PARAMETERS structure](..\xapo\ns-xapo-xapo_process_buffer_parameters.md) | Defines stream buffer parameters that may change from one call to the next. Used with the Process method. |
| [XAPO_REGISTRATION_PROPERTIES structure](..\xapo\ns-xapo-xapo_registration_properties.md) | Describes general characteristics of an XAPO. Used with IXAPO |
| [XAUDIO2FX_REVERB_I3DL2_PARAMETERS structure](..\xaudio2fx\ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters.md) | Describes I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters for use in the ReverbConvertI3DL2ToNative function. |
| [XAUDIO2FX_REVERB_PARAMETERS structure](..\xaudio2fx\ns-xaudio2fx-xaudio2fx_reverb_parameters.md) | Describes parameters for use in the reverb APO. |
| [XAUDIO2FX_VOLUMEMETER_LEVELS structure](..\xaudio2fx\ns-xaudio2fx-xaudio2fx_volumemeter_levels.md) | Describes parameters for use with the volume meter APO. |
| [XAUDIO2_BUFFER structure](..\xaudio2\ns-xaudio2-xaudio2_buffer.md) | Represents an audio data buffer, used with IXAudio2SourceVoice |
| [XAUDIO2_BUFFER_WMA structure](..\xaudio2\ns-xaudio2-xaudio2_buffer_wma.md) | Used with IXAudio2SourceVoice |
| [XAUDIO2_DEBUG_CONFIGURATION structure](..\xaudio2\ns-xaudio2-xaudio2_debug_configuration.md) | Contains the new global debug configuration for XAudio2. Used with the SetDebugConfiguration function. |
| [XAUDIO2_EFFECT_CHAIN structure](..\xaudio2\ns-xaudio2-xaudio2_effect_chain.md) | Defines an effect chain. |
| [XAUDIO2_EFFECT_DESCRIPTOR structure](..\xaudio2\ns-xaudio2-xaudio2_effect_descriptor.md) | Contains information about an XAPO for use in an effect chain. |
| [XAUDIO2_FILTER_PARAMETERS structure](..\xaudio2\ns-xaudio2-xaudio2_filter_parameters.md) | Defines filter parameters for a source voice. |
| [XAUDIO2_PERFORMANCE_DATA structure](..\xaudio2\ns-xaudio2-xaudio2_performance_data.md) | Contains performance information. |
| [XAUDIO2_SEND_DESCRIPTOR structure](..\xaudio2\ns-xaudio2-xaudio2_send_descriptor.md) | Defines a destination voice that is the target of a send from another voice and specifies whether a filter should be used. |
| [XAUDIO2_VOICE_DETAILS structure](..\xaudio2\ns-xaudio2-xaudio2_voice_details.md) | Contains information about the creation flags, input channels, and sample rate of a voice. |
| [XAUDIO2_VOICE_SENDS structure](..\xaudio2\ns-xaudio2-xaudio2_voice_sends.md) | Defines a set of voices to receive data from a single output voice. |
| [XAUDIO2_VOICE_STATE structure](..\xaudio2\ns-xaudio2-xaudio2_voice_state.md) | Returns the voice's current state and cursor position data. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [HrtfDirectivityType enumeration](..\hrtfapoapi\ne-hrtfapoapi-hrtfdirectivitytype.md) | Indicates one of several stock directivity patterns. |
| [HrtfDistanceDecayType enumeration](..\hrtfapoapi\ne-hrtfapoapi-hrtfdistancedecaytype.md) | Indicates a distance-based decay type applied to a sound. |
| [HrtfEnvironment enumeration](..\hrtfapoapi\ne-hrtfapoapi-hrtfenvironment.md) | Indicates one of several stock environment types. |
| [XAPO_BUFFER_FLAGS enumeration](..\xapo\ne-xapo-xapo_buffer_flags.md) | Describes the contents of a stream buffer. |
| [XAUDIO2_FILTER_TYPE enumeration](..\xaudio2\ne-xaudio2-xaudio2_filter_type.md) | Indicates the filter type. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IXAPO interface](..\xapo\nn-xapo-ixapo.md) | The interface for an Audio Processing Object which be used in an XAudio2 effect chain. |
| [IXAPOParameters interface](..\xapo\nn-xapo-ixapoparameters.md) | An optional interface that allows an XAPO to use effect-specific parameters. |
| [IXAudio2 interface](..\xaudio2\nn-xaudio2-ixaudio2.md) | IXAudio2 is the interface for the XAudio2 object that manages all audio engine states, the audio processing thread, the voice graph, and so forth. |
| [IXAudio2EngineCallback interface](..\xaudio2\nn-xaudio2-ixaudio2enginecallback.md) | The IXAudio2EngineCallback interface contains methods that notify the client when certain events happen in the IXAudio2 engine. |
| [IXAudio2MasteringVoice interface](..\xaudio2\nn-xaudio2-ixaudio2masteringvoice.md) | A mastering voice is used to represent the audio output device. |
| [IXAudio2SourceVoice interface](..\xaudio2\nn-xaudio2-ixaudio2sourcevoice.md) | Use a source voice to submit audio data to the XAudio2 processing pipeline. |
| [IXAudio2SubmixVoice interface](..\xaudio2\nn-xaudio2-ixaudio2submixvoice.md) | A submix voice is used primarily for performance improvements and effects processing. |
| [IXAudio2Voice interface](..\xaudio2\nn-xaudio2-ixaudio2voice.md) | IXAudio2Voice represents the base interface from which IXAudio2SourceVoice, IXAudio2SubmixVoice and IXAudio2MasteringVoice are derived. The methods listed below are common to all voice subclasses. |
| [IXAudio2VoiceCallback interface](..\xaudio2\nn-xaudio2-ixaudio2voicecallback.md) | The IXAudio2VoiceCallback interface contains methods that notify the client when certain events happen in a given IXAudio2SourceVoice. |

## Classes

| Title   | Description   |
| ---- |:---- |
| [CXAPOBase class](..\xapobase\nl-xapobase-cxapobase.md) | Default implementation of the IXAPO interface. |
| [CXAPOParametersBase class](..\xapobase\nl-xapobase-cxapoparametersbase.md) | Default implementation of the IXAPOParameters interface. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [XAPOAlloc macro](..\xapo\nf-xapo-xapoalloc.md) | Memory allocation macro used by IXAPO methods that must allocate arbitrary sized structures that are subsequently returned to the application. |
| [XAPOFree macro](..\xapo\nf-xapo-xapofree.md) | Macro used to free memory allocated with the XAPOAlloc macro. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [CXAPOBase::CXAPOBase](..\xapobase\nf-xapobase-cxapobase-cxapobase.md) | Creates an instance of the CXAPOBase class. |
| [CXAPOBase::GetRegistrationPropertiesInternal](..\xapobase\nf-xapobase-cxapobase-getregistrationpropertiesinternal.md) | Returns a pointer to the XAPO_REGISTRATION_PROPERTIES structure containing the registration properties the XAPO was created with. |
| [CXAPOBase::IsLocked](..\xapobase\nf-xapobase-cxapobase-islocked.md) | Queries whether the XAPO is locked. |
| [CXAPOBase::ProcessThru](..\xapobase\nf-xapobase-cxapobase-processthru.md) | Called by an IXAPO |
| [CXAPOBase::ValidateFormatDefault](..\xapobase\nf-xapobase-cxapobase-validateformatdefault.md) | Verifies that an audio format falls within the default ranges supported. |
| [CXAPOBase::ValidateFormatPair](..\xapobase\nf-xapobase-cxapobase-validateformatpair.md) | Verifies that an input and output format pair configuration is supported by the XAPO. |
| [CXAPOParametersBase::BeginProcess](..\xapobase\nf-xapobase-cxapoparametersbase-beginprocess.md) | Returns the current process parameters. |
| [CXAPOParametersBase::CXAPOParametersBase](..\xapobase\nf-xapobase-cxapoparametersbase-cxapoparametersbase.md) | Creates an instance of the CXAPOParametersBase class. |
| [CXAPOParametersBase::EndProcess](..\xapobase\nf-xapobase-cxapoparametersbase-endprocess.md) | Notifies CXAPOParametersBase that the XAPO has finished accessing the current process parameters. |
| [CXAPOParametersBase::OnSetParameters](..\xapobase\nf-xapobase-cxapoparametersbase-onsetparameters.md) | Called by IXAPOParameters |
| [CXAPOParametersBase::ParametersChanged](..\xapobase\nf-xapobase-cxapoparametersbase-parameterschanged.md) | Indicates if IXAPOParameters |
| [IXAPO::CalcInputFrames](..\xapo\nf-xapo-ixapo-calcinputframes.md) | Returns the number of input frames required to generate the given number of output frames. |
| [IXAPO::CalcOutputFrames](..\xapo\nf-xapo-ixapo-calcoutputframes.md) | Returns the number of output frames that will be generated from a given number of input frames. |
| [IXAPO::GetRegistrationProperties](..\xapo\nf-xapo-ixapo-getregistrationproperties.md) | Returns the registration properties of an XAPO. |
| [IXAPO::Initialize](..\xapo\nf-xapo-ixapo-initialize.md) | Performs any effect-specific initialization. |
| [IXAPO::IsInputFormatSupported](..\xapo\nf-xapo-ixapo-isinputformatsupported.md) | Queries if a specific input format is supported for a given output format. |
| [IXAPO::IsOutputFormatSupported](..\xapo\nf-xapo-ixapo-isoutputformatsupported.md) | Queries if a specific output format is supported for a given input format. |
| [IXAPO::LockForProcess](..\xapo\nf-xapo-ixapo-lockforprocess.md) | Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before Process is called on the realtime thread. |
| [IXAPO::Process](..\xapo\nf-xapo-ixapo-process.md) | Runs the XAPO's digital signal processing (DSP) code on the given input and output buffers. |
| [IXAPO::Reset](..\xapo\nf-xapo-ixapo-reset.md) | Resets variables dependent on frame history. |
| [IXAPO::UnlockForProcess](..\xapo\nf-xapo-ixapo-unlockforprocess.md) | Deallocates variables that were allocated with the LockForProcess method. |
| [IXAPOParameters::GetParameters](..\xapo\nf-xapo-ixapoparameters-getparameters.md) | Gets the current values for any effect-specific parameters. |
| [IXAPOParameters::SetParameters](..\xapo\nf-xapo-ixapoparameters-setparameters.md) | Sets effect-specific parameters. |
| [IXAudio2::AddRef](..\xaudio2\nf-xaudio2-ixaudio2-addref.md) | Adds a reference to the XAudio2 object. |
| [IXAudio2::CommitChanges](..\xaudio2\nf-xaudio2-ixaudio2-commitchanges.md) | Atomically applies a set of operations that are tagged with a given identifier. |
| [IXAudio2::CreateMasteringVoice](..\xaudio2\nf-xaudio2-ixaudio2-createmasteringvoice.md) | Creates and configures a mastering voice. |
| [IXAudio2::CreateSourceVoice](..\xaudio2\nf-xaudio2-ixaudio2-createsourcevoice.md) | Creates and configures a source voice. |
| [IXAudio2::CreateSubmixVoice](..\xaudio2\nf-xaudio2-ixaudio2-createsubmixvoice.md) | Creates and configures a submix voice. |
| [IXAudio2::GetPerformanceData](..\xaudio2\nf-xaudio2-ixaudio2-getperformancedata.md) | Returns current resource usage details, such as available memory or CPU usage. |
| [IXAudio2::QueryInterface](..\xaudio2\nf-xaudio2-ixaudio2-queryinterface.md) | Queries for a given COM interface on the XAudio2 object. |
| [IXAudio2::RegisterForCallbacks](..\xaudio2\nf-xaudio2-ixaudio2-registerforcallbacks.md) | Adds an IXAudio2EngineCallback pointer to the XAudio2 engine callback list. |
| [IXAudio2::Release](..\xaudio2\nf-xaudio2-ixaudio2-release.md) | Releases a reference to the XAudio2 object. |
| [IXAudio2::SetDebugConfiguration](..\xaudio2\nf-xaudio2-ixaudio2-setdebugconfiguration.md) | Changes global debug logging options for XAudio2. |
| [IXAudio2::StartEngine](..\xaudio2\nf-xaudio2-ixaudio2-startengine.md) | Starts the audio processing thread. |
| [IXAudio2::StopEngine](..\xaudio2\nf-xaudio2-ixaudio2-stopengine.md) | Stops the audio processing thread. |
| [IXAudio2::UnregisterForCallbacks](..\xaudio2\nf-xaudio2-ixaudio2-unregisterforcallbacks.md) | Removes an IXAudio2EngineCallback pointer from the XAudio2 engine callback list. |
| [IXAudio2EngineCallback::OnCriticalError](..\xaudio2\nf-xaudio2-ixaudio2enginecallback-oncriticalerror.md) | Called if a critical system error occurs that requires XAudio2 to be closed down and restarted. |
| [IXAudio2EngineCallback::OnProcessingPassEnd](..\xaudio2\nf-xaudio2-ixaudio2enginecallback-onprocessingpassend.md) | Called by XAudio2 just after an audio processing pass ends. |
| [IXAudio2EngineCallback::OnProcessingPassStart](..\xaudio2\nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart.md) | Called by XAudio2 just before an audio processing pass begins. |
| [IXAudio2MasteringVoice::GetChannelMask](..\xaudio2\nf-xaudio2-ixaudio2masteringvoice-getchannelmask.md) | Returns the channel mask for this voice. |
| [IXAudio2SourceVoice::Discontinuity](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-discontinuity.md) | Notifies an XAudio2 voice that no more buffers are coming after the last one that is currently in its queue. |
| [IXAudio2SourceVoice::ExitLoop](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-exitloop.md) | Stops looping the voice when it reaches the end of the current loop region. |
| [IXAudio2SourceVoice::FlushSourceBuffers](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-flushsourcebuffers.md) | Removes all pending audio buffers from the voice queue. |
| [IXAudio2SourceVoice::GetFrequencyRatio](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-getfrequencyratio.md) | Returns the frequency adjustment ratio of the voice. |
| [IXAudio2SourceVoice::GetState](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-getstate.md) | Returns the voice's current cursor position data. |
| [IXAudio2SourceVoice::SetFrequencyRatio](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio.md) | Sets the frequency adjustment ratio of the voice. |
| [IXAudio2SourceVoice::SetSourceSampleRate](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-setsourcesamplerate.md) | Reconfigures the voice to consume source data at a different sample rate than the rate specified when the voice was created. |
| [IXAudio2SourceVoice::Start](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-start.md) | Starts consumption and processing of audio by the voice. Delivers the result to any connected submix or mastering voices, or to the output device. |
| [IXAudio2SourceVoice::Stop](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-stop.md) | Stops consumption of audio by the current voice. |
| [IXAudio2SourceVoice::SubmitSourceBuffer](..\xaudio2\nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer.md) | Adds a new audio buffer to the voice queue. |
| [IXAudio2VoiceCallback::OnBufferEnd](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onbufferend.md) | Called when the voice finishes processing a buffer. |
| [IXAudio2VoiceCallback::OnBufferStart](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onbufferstart.md) | Called when the voice is about to start processing a new audio buffer. |
| [IXAudio2VoiceCallback::OnLoopEnd](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onloopend.md) | Called when the voice reaches the end position of a loop. |
| [IXAudio2VoiceCallback::OnStreamEnd](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onstreamend.md) | Called when the voice has just finished playing a contiguous audio stream. |
| [IXAudio2VoiceCallback::OnVoiceError](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onvoiceerror.md) | Called when a critical error occurs during voice processing. |
| [IXAudio2VoiceCallback::OnVoiceProcessingPassEnd](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onvoiceprocessingpassend.md) | Called just after the processing pass for the voice ends. |
| [IXAudio2VoiceCallback::OnVoiceProcessingPassStart](..\xaudio2\nf-xaudio2-ixaudio2voicecallback-onvoiceprocessingpassstart.md) | Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue. |
