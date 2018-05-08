---
UID: NF:mswmdm.IMDSPDeviceControl.Play
title: IMDSPDeviceControl::Play
author: windows-driver-content
description: The Play method begins playing at the current seek position. If the Seek method has not been called, then playing begins at the beginning of the first file, and the play length is not defined.
old-location: wmdm\imdspdevicecontrol_play.htm
old-project: WMDM
ms.assetid: 09ca1922-3b33-47a8-a851-a1d221a568b9
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IMDSPDeviceControl interface [windows Media Device Manager],Play method, IMDSPDeviceControl.Play, IMDSPDeviceControl::Play, IMDSPDeviceControlPlay, Play, Play method [windows Media Device Manager], Play method [windows Media Device Manager],IMDSPDeviceControl interface, mswmdm/IMDSPDeviceControl::Play, wmdm.imdspdevicecontrol_play
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IMDSPDeviceControl.Play
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPDeviceControl::Play


## -description



The <b>Play</b> method begins playing at the current seek position. If the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a> method has not been called, then playing begins at the beginning of the first file, and the play length is not defined.




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



This method is used to invoke both device playback (playback of an audio track on a storage medium of the media device) and streaming audio playback (streaming audio data from the user's computer to the media device, where it is played). The <b>Seek</b> method determines the form of playback that occurs.

Some devices do not support either device playback or streaming audio playback. Before attempting to start playback of a particular type, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a> method must be called. If unsupported playback is attempted, this method returns WMDM_E_NOTSUPPORTED.

To determine whether an audio format can be played by the media device before invoking the play operation, you can call the <a href="https://msdn.microsoft.com/ac50ac7d-bd55-4ece-8af8-5c8b2f7736e8">IMDSPDevice::GetFormatSupport</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ac50ac7d-bd55-4ece-8af8-5c8b2f7736e8">IMDSPDevice::GetFormatSupport</a>



<a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/5d4e433a-fb2a-43c4-ab7f-fb7168636455">IMDSPDeviceControl::GetCapabilities</a>



<a href="https://msdn.microsoft.com/05fbaab8-e1fa-4960-9591-d22347bc04f2">IMDSPDeviceControl::Seek</a>
 

 

