---
UID: TP:mediastreaming
ms.assetid: 657c5a21-72d5-3f12-a0eb-79444b5e3ef4
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Media Streaming API



Overview of the Media Streaming API technology.

To develop Media Streaming API, you need these headers:

 * [windows.media.streaming.h](..\windows.media.streaming\index.md)

For the programming guide, see [Media Streaming API](/windows/desktop/mediastreaming).

## Structures

| Title   | Description   |
| ---- |:---- |
| [PlaySpeed structure](..\windows.media.streaming\ns-windows-media-streaming-playspeed.md) | Represents a playback speed as a rational number. |
| [PositionInformation structure](..\windows.media.streaming\ns-windows-media-streaming-positioninformation.md) | Contains the current values of media playback position information obtained from the DMR. |
| [RenderingParameters structure](..\windows.media.streaming\ns-windows-media-streaming-renderingparameters.md) | Contains the current values of rendering parameters on the DMR. |
| [TrackInformation structure](..\windows.media.streaming\ns-windows-media-streaming-trackinformation.md) | Contains the current track number and duration as part of the PositionInformation obtained from the DMR. |
| [TransportInformation structure](..\windows.media.streaming\ns-windows-media-streaming-transportinformation.md) | Contains the current values of media playback transport-related information obtained from the DMR. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDeviceController interface](..\windows.media.streaming\nn-windows-media-streaming-idevicecontroller.md) | Encapsulates the methods and events needed to retrieve a list of cached Digital Media Renderers (DMRs) and/or Digital Media Servers (DMSs), or to asynchronously find the DMRs and/or DMSs that are currently on the network. |
| [IDeviceIcon interface](..\windows.media.streaming\nn-windows-media-streaming-ideviceicon.md) | Encapsulates the methods needed to provide information about the icon of a DLNA Device. |
| [IMediaRendererActionInformation interface](..\windows.media.streaming\nn-windows-media-streaming-imediarendereractioninformation.md) | Encapsulates the methods needed to provide information about what methods can currently be invoked on the DMR. |
| [IMediaRendererFactory interface](..\windows.media.streaming\nn-windows-media-streaming-imediarendererfactory.md) | Encapsulates the methods needed to asynchronously create a new instance of an object that implements the IMediaRenderer interface. |
| [IStreamSelectorStatics interface](..\windows.media.streaming\nn-windows-media-streaming-istreamselectorstatics.md) | Encapsulates the methods needed to asynchronously select a stream. |
| [ITransportParameters interface](..\windows.media.streaming\nn-windows-media-streaming-itransportparameters.md) | Encapsulates the methods needed to provide information about the current transport-related settings of the DMR. These settings include the current transport state and information about what methods can currently be invoked on the DMR. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDeviceController::streaming](..\windows.media.streaming\nf-windows-media-streaming-idevicecontroller-add_devicearrival.md) | Registers an event handler for the DeviceArrival event. |
| [IDeviceController::streaming](..\windows.media.streaming\nf-windows-media-streaming-idevicecontroller-add_devicedeparture.md) | Registers an event handler for the DeviceDeparture event. |
| [IDeviceController::streaming](..\windows.media.streaming\nf-windows-media-streaming-idevicecontroller-adddevice.md) | Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the CachedDevices method. |
| [IDeviceController::streaming](..\windows.media.streaming\nf-windows-media-streaming-idevicecontroller-remove_devicearrival.md) | Unregisters an event handler for the DeviceArrival event. |
| [IDeviceController::streaming](..\windows.media.streaming\nf-windows-media-streaming-idevicecontroller-remove_devicedeparture.md) | Unregisters an event handler for the DeviceDeparture event. |
| [IDeviceController::streaming](..\windows.media.streaming\nf-windows-media-streaming-idevicecontroller-removedevice.md) | Removes the specified device from the list of devices that is returned by the CachedDevices method. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate.md) | Registers an event handler for the RenderingParametersUpdate event. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-add_transportparametersupdate.md) | Registers an event handler for the TransportParametersUpdate event. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-getmuteasync.md) | Queries the DMR asynchronously to determine if audio is currently muted or unmuted. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-getpositioninformationasync.md) | Queries the DMR asynchronously to retrieve position information. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-gettransportinformationasync.md) | Queries the DMR asynchronously to retrieve transport information. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-getvolumeasync.md) | Queries the DMR asynchronously for its current audio volume level. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-playasync.md) | Instructs the DMR asynchronously to play the content that was specified by calling the SetSourceFromUriAsync, SetSourceFromStreamAsync, or SetSourceFromMediaSourceAsync method. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-playatspeedasync.md) | Instructs the DMR asynchronously to play the content that was specified by calling the SetSourceFromUriAsync, SetSourceFromStreamAsync, or SetSourceFromMediaSourceAsync method at the specified rate. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate.md) | Unregisters an event handler for the RenderingParametersUpdate event. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate.md) | Unregisters an event handler for the TransportParametersUpdate event. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-seekasync.md) | Instructs the DMR asynchronously to seek to a particular time offset. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setmuteasync.md) | Instructs the DMR asynchronously to either mute or unmute the audio. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync.md) | Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync.md) | Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync.md) | Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing once the current content has finished playing. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync.md) | Instructs the DMR asynchronously to prepare the specified content for playing. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync.md) | Instructs the DMR asynchronously to prepare the specified media stream for playing. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setsourcefromuriasync.md) | Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing. |
| [IMediaRenderer::streaming](..\windows.media.streaming\nf-windows-media-streaming-imediarenderer-setvolumeasync.md) | Sets the audio volume level on the DMR asynchronously to the specified value. |
| [IStreamSelectorStatics::streaming](..\windows.media.streaming\nf-windows-media-streaming-istreamselectorstatics-getstreampropertiesasync.md) | When implemented gets the properties of the stream asynchronously. |
| [IStreamSelectorStatics::streaming](..\windows.media.streaming\nf-windows-media-streaming-istreamselectorstatics-selectbeststreamasync.md) | When implemented queries asynchronously for the best stream. |
