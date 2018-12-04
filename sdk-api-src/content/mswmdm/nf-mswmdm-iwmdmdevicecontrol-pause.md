---
UID: NF:mswmdm.IWMDMDeviceControl.Pause
title: IWMDMDeviceControl::Pause
author: windows-sdk-content
description: The Pause method pauses the current play or record session at the current position within the content.
old-location: wmdm\iwmdmdevicecontrol_pause.htm
tech.root: WMDM
ms.assetid: 420963d1-11ea-4f1d-b5c0-749e99ee7725
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Pause method, IWMDMDeviceControl.Pause, IWMDMDeviceControl::Pause, IWMDMDeviceControlPause, Pause, Pause method [windows Media Device Manager], Pause method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Pause, wmdm.iwmdmdevicecontrol_pause
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDeviceControl.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDeviceControl::Pause


## -description



The <b>Pause</b> method pauses the current play or record session at the current position within the content.




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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The device is already paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The pause function is not implemented on this device.

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



The current playback or record session is paused and the current file position is saved. A subsequent call to the <a href="https://msdn.microsoft.com/24ee343c-09ed-4a5f-b7be-eba15dcc4b36">Resume</a> method restarts the play or record operation at the saved file position.




## -see-also




<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

