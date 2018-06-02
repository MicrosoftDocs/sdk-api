---
UID: TP:wia
ms.assetid: 3aacaecd-d808-35d7-b283-04705ef2fdca
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# WIA



Overview of the WIA technology.

To develop WIA, you need these headers:

 * [wiadef.h](..\wiadef\index.md)
 * [wiadevd.h](..\wiadevd\index.md)
 * [wiavideo.h](..\wiavideo\index.md)

For the programming guide, see [WIA](/windows/desktop/wia).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DeviceDialog function](..\wiadevd\nf-wiadevd-devicedialog.md) | Used by applications to display a device dialog box to the user. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_WIA_RAW_HEADER structure](..\wiadef\ns-wiadef-_wia_raw_header.md) | The WIA_RAW_HEADER structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [__MIDL___MIDL_itf_wiavideo_xp_0000_0000_0001 enumeration](..\wiavideo\ne-wiavideo-__midl___midl_itf_wiavideo_xp_0000_0000_0001.md) | The WIAVIDEO_STATE enumeration is used to specify the current state of a video stream. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IWiaVideo interface](..\wiavideo\nn-wiavideo-iwiavideo.md) | The IWiaVideo interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.Note  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use DirectShow to acquire images from video. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IWiaVideo::CreateVideoByDevNum](..\wiavideo\nf-wiavideo-iwiavideo-createvideobydevnum.md) | The IWiaVideo |
| [IWiaVideo::CreateVideoByName](..\wiavideo\nf-wiavideo-iwiavideo-createvideobyname.md) | The IWiaVideo |
| [IWiaVideo::CreateVideoByWiaDevID](..\wiavideo\nf-wiavideo-iwiavideo-createvideobywiadevid.md) | The IWiaVideo |
| [IWiaVideo::DestroyVideo](..\wiavideo\nf-wiavideo-iwiavideo-destroyvideo.md) | The IWiaVideo |
| [IWiaVideo::GetCurrentState](..\wiavideo\nf-wiavideo-iwiavideo-getcurrentstate.md) | The IWiaVideo |
| [IWiaVideo::Pause](..\wiavideo\nf-wiavideo-iwiavideo-pause.md) | The IWiaVideo |
| [IWiaVideo::Play](..\wiavideo\nf-wiavideo-iwiavideo-play.md) | Begins playback of streaming video. |
| [IWiaVideo::ResizeVideo](..\wiavideo\nf-wiavideo-iwiavideo-resizevideo.md) | The IWiaVideo |
| [IWiaVideo::TakePicture](..\wiavideo\nf-wiavideo-iwiavideo-takepicture.md) | The IWiaVideo |
| [IWiaVideo::get_ImagesDirectory](..\wiavideo\nf-wiavideo-iwiavideo-get_imagesdirectory.md) | The IWiaVideo |
| [IWiaVideo::get_PreviewVisible](..\wiavideo\nf-wiavideo-iwiavideo-get_previewvisible.md) | The IWiaVideo |
| [IWiaVideo::put_ImagesDirectory](..\wiavideo\nf-wiavideo-iwiavideo-put_imagesdirectory.md) | The IWiaVideo |
| [IWiaVideo::put_PreviewVisible](..\wiavideo\nf-wiavideo-iwiavideo-put_previewvisible.md) | The IWiaVideo |
