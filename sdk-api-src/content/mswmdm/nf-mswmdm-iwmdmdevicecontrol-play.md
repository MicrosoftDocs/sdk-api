---
UID: NF:mswmdm.IWMDMDeviceControl.Play
title: IWMDMDeviceControl::Play
author: windows-sdk-content
description: The Play method begins playing at the current seek position. If the IWMDMDeviceControl::Seek method has not been called, then playing begins at the beginning of the first file, and the play length is not defined.
old-location: wmdm\iwmdmdevicecontrol_play.htm
old-project: WMDM
ms.assetid: e8d717e6-365c-44ad-b24e-daa3c35664de
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Play method, IWMDMDeviceControl.Play, IWMDMDeviceControl::Play, IWMDMDeviceControlPlay, Play, Play method [windows Media Device Manager], Play method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Play, wmdm.iwmdmdevicecontrol_play
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDeviceControl.Play
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDeviceControl::Play


## -description



The <b>Play</b> method begins playing at the current seek position. If the <b>IWMDMDeviceControl::Seek</b> method has not been called, then playing begins at the beginning of the first file, and the play length is not defined.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The device is busy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The play function is not implemented on this device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



This method is used to invoke both device playback (playing an audio track on a storage medium of the media device) and streaming audio playback (streaming audio data from the user's computer to the media device, where it is played). The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a> method determines the form of playback that occurs.

Some devices do not support either device playback or streaming audio playback. Before attempting to start playback of a particular type, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a> method must be called. If unsupported playback is attempted, this method returns WMDM_E_NOTSUPPORTED.

To determine before invoking the play operation whether an audio format can be played by the media device, you can call the <a href="https://msdn.microsoft.com/a917660d-300f-4ac4-befe-a3f78172411e">GetFormatSupport</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a917660d-300f-4ac4-befe-a3f78172411e">IWMDMDevice::GetFormatSupport</a>



<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/61d0e44c-f1be-4837-a773-48c6c5278fe0">IWMDMDeviceControl::GetCapabilities</a>



<a href="https://msdn.microsoft.com/f416a520-197c-4607-979e-8f43951f2076">IWMDMDeviceControl::Seek</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

