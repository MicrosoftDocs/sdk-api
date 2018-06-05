---
UID: NF:mswmdm.IWMDMDeviceControl.GetStatus
title: IWMDMDeviceControl::GetStatus
author: windows-sdk-content
description: The GetStatus method retrieves the control status of the device.
old-location: wmdm\iwmdmdevicecontrol_getstatus.htm
old-project: WMDM
ms.assetid: e39fb2ed-a3b4-4167-9404-6b7c706f0941
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IWMDMDeviceControl interface, IWMDMDeviceControl interface [windows Media Device Manager],GetStatus method, IWMDMDeviceControl.GetStatus, IWMDMDeviceControl::GetStatus, IWMDMDeviceControlGetDCStatus, mswmdm/IWMDMDeviceControl::GetStatus, wmdm.iwmdmdevicecontrol_getstatus
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMDeviceControl.GetStatus
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDeviceControl::GetStatus


## -description



The <b>GetStatus</b> method retrieves the control status of the device.




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> that specifies the control status of the device. The control status value specifies one or more of the following flags.

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



This call returns status values specific to the device control operations of this interface. The control status can provide information about the state of control-related activities of the device, such as playing, recording, and so on. However, it cannot provide information about the global status of the device, such as whether the device is downloading data or being accessed for some other reason. If the device is busy for any reason other than device control, you receive a busy code and must call the <a href="https://msdn.microsoft.com/18445ba5-6c91-4b4c-8f9b-b9d94fd96155">IWMDMDeviceControl::GetStatus</a> method for more detailed information.

You must not attempt to call the <a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a>, <a href="https://msdn.microsoft.com/a9372ce9-e339-4664-9e12-4feae29529dc">Record</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>, <a href="https://msdn.microsoft.com/24ee343c-09ed-4a5f-b7be-eba15dcc4b36">Resume</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a> methods of this interface if the status value WMDM_STATUS_BUSY is returned and the status value does not contain any other values from the table of status values.




## -see-also




<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

