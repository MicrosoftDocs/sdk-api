---
UID: NF:mswmdm.IMDSPDeviceControl.Record
title: IMDSPDeviceControl::Record
author: windows-sdk-content
description: The Record method begins recording from the device's external record input at the current seek position. The Seek method must be called first.
old-location: wmdm\imdspdevicecontrol_record.htm
tech.root: WMDM
ms.assetid: 6cd99cfc-1961-4369-9ce9-2cdd0136d181
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMDSPDeviceControl interface [windows Media Device Manager],Record method, IMDSPDeviceControl.Record, IMDSPDeviceControl::Record, IMDSPDeviceControlRecord, Record, Record method [windows Media Device Manager], Record method [windows Media Device Manager],IMDSPDeviceControl interface, mswmdm/IMDSPDeviceControl::Record, wmdm.imdspdevicecontrol_record
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
 - IMDSPDeviceControl.Record
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IMDSPDeviceControl.Record
: 
---

# IMDSPDeviceControl::Record


## -description



The <b>Record</b> method begins recording from the device's external record input at the current seek position. The <a href="https://msdn.microsoft.com/05fbaab8-e1fa-4960-9591-d22347bc04f2">Seek</a> method must be called first.




## -parameters




### -param pFormat [in]

Pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure containing the format in which the data must be recorded.


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
The device is already performing an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The record function is not implemented on this device.

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



This method is used to invoke both device recording (recording of an audio track to be stored on the media device) and streaming audio data from the media device to be recorded on the computer. The <b>Seek</b> method determines which form of recording occurs.

Some devices do not support either type of recording. The <a href="https://msdn.microsoft.com/5d4e433a-fb2a-43c4-ab7f-fb7168636455">GetCapabilities</a> method must be called before you start recording. If an unsupported type of recording is attempted, this method returns WMDM_E_NOTSUPPORTED.

An argument for the <i>pFormat</i> parameter can be supplied to specify an audio data format for recording. To determine the formats supported by the device, see <a href="https://msdn.microsoft.com/ac50ac7d-bd55-4ece-8af8-5c8b2f7736e8">IMDSPDevice::GetFormatSupport</a>. If the <i>pFormat</i> parameter is set to <b>NULL</b>, the device records audio data in the default format.

When you use device recording, you must enumerate the storage medium contents to find the new object after the record operation is finished.




## -see-also




<a href="https://msdn.microsoft.com/ac50ac7d-bd55-4ece-8af8-5c8b2f7736e8">IMDSPDevice::GetFormatSupport</a>



<a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/5d4e433a-fb2a-43c4-ab7f-fb7168636455">IMDSPDeviceControl::GetCapabilities</a>



<a href="https://msdn.microsoft.com/05fbaab8-e1fa-4960-9591-d22347bc04f2">IMDSPDeviceControl::Seek</a>



<a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a>
 

 

