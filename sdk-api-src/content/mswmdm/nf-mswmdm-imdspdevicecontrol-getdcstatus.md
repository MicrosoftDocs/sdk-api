---
UID: NF:mswmdm.IMDSPDeviceControl.GetDCStatus
title: IMDSPDeviceControl::GetDCStatus
author: windows-driver-content
description: The GetDCStatus method retrieves the control status of the device.
old-location: wmdm\imdspdevicecontrol_getdcstatus.htm
old-project: WMDM
ms.assetid: 6fc51100-3052-4d26-8786-a7b1e9fe0529
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetDCStatus, GetDCStatus method [windows Media Device Manager], GetDCStatus method [windows Media Device Manager],IMDSPDeviceControl interface, IMDSPDeviceControl interface [windows Media Device Manager],GetDCStatus method, IMDSPDeviceControl.GetDCStatus, IMDSPDeviceControl::GetDCStatus, IMDSPDeviceControlGetDCStatus, mswmdm/IMDSPDeviceControl::GetDCStatus, wmdm.imdspdevicecontrol_getdcstatus
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
-	IMDSPDeviceControl.GetDCStatus
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPDeviceControl::GetDCStatus


## -description



The <b>GetDCStatus</b> method retrieves the control status of the device.




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> that contains the control status of the device. The control status value contains one or more of the following flags.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_STATUS_READY</td>
<td>Windows Media Device Manager and its subcomponents are in a ready state.</td>
</tr>
<tr>
<td>WMDM_STATUS_BUSY</td>
<td>An operation is currently being performed. Evaluate the other status values to determine which operation it is.</td>
</tr>
<tr>
<td>WMDM_STATUS_DEVICECONTROL_PLAYING</td>
<td>The device is currently playing.</td>
</tr>
<tr>
<td>WMDM_STATUS_DEVICECONTROL_RECORDING</td>
<td>The device is currently recording.</td>
</tr>
<tr>
<td>WMDM_STATUS_DEVICECONTROL_PAUSED</td>
<td>The device is currently paused.</td>
</tr>
<tr>
<td>WMDM_STATUS_DEVICECONTROL_REMOTE</td>
<td>The play or record operation of the device is being remotely controlled by the application.</td>
</tr>
<tr>
<td>WMDM_STATUS_DEVICECONTROL_STREAM</td>
<td>The play or record method is streaming data to or from the media device.</td>
</tr>
</table>
 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwStatus</i> parameter is an invalid or <b>NULL</b> pointer.

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



This call returns status values specific to the device control operations of this interface. The control status can provide information about the state of control-related activities of the device, such as playing, recording, and so on. However, it cannot provide information about the global status of the device, such as whether the device is downloading data or being accessed for some other reason. If the device is busy for any reason other than device control, you receive a busy code and must call the <b>GetStatus</b> method of the associated <b>IMDSPDevice</b> interface for more detailed information.

You must not attempt to call the <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">Play</a>, <a href="https://msdn.microsoft.com/6cd99cfc-1961-4369-9ce9-2cdd0136d181">Record</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>, <a href="https://msdn.microsoft.com/6c7e26dc-05cd-4dfd-86c8-0b7b216b6772">Resume</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a> methods of this interface if the status value WMDM_STATUS_BUSY is returned and the status value does not contain any other values from the table of status values.




## -see-also




<a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl Interface</a>
 

 

