---
UID: NF:mswmdm.IWMDMDeviceControl.Record
title: IWMDMDeviceControl::Record (mswmdm.h)
author: windows-sdk-content
description: The Record method begins recording from the device's external record input at the current seek position. The IWMDMDeviceControl::Seek method must be called first.
old-location: wmdm\iwmdmdevicecontrol_record.htm
tech.root: WMDM
ms.assetid: a9372ce9-e339-4664-9e12-4feae29529dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Record method, IWMDMDeviceControl.Record, IWMDMDeviceControl::Record, IWMDMDeviceControlRecord, Record, Record method [windows Media Device Manager], Record method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Record, wmdm.iwmdmdevicecontrol_record
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
 - IWMDMDeviceControl.Record
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDeviceControl::Record


## -description



The <b>Record</b> method begins recording from the device's external record input at the current seek position. The <b>IWMDMDeviceControl::Seek</b> method must be called first.




## -parameters




### -param pFormat [in]

Pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure specifying the format in which the data must be recorded.


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



This method is used to invoke both device recording (recording of an audio track to be stored on the media device) and streaming audio data from the media device to be recorded on the computer. The <a href="https://msdn.microsoft.com/f416a520-197c-4607-979e-8f43951f2076">Seek</a> method determines which form of recording occurs.

Some devices do not support either type of recording. The <a href="https://msdn.microsoft.com/61d0e44c-f1be-4837-a773-48c6c5278fe0">GetCapabilities</a> method must be called before you start recording. If an unsupported type of recording is attempted, this method returns WMDM_E_NOTSUPPORTED.

An argument can be supplied for the <i>pFormat</i> parameter to specify an audio format for recording. To determine the formats supported by the device, see <a href="https://msdn.microsoft.com/a917660d-300f-4ac4-befe-a3f78172411e">GetFormatSupport</a>. If the <i>pFormat</i> parameter is set to <b>NULL</b>, the device records audio data in the default format.

When you use device recording, you must enumerate the storage medium contents to find the new object after the record operation is finished.




## -see-also




<a href="https://msdn.microsoft.com/a917660d-300f-4ac4-befe-a3f78172411e">IWMDMDevice::GetFormatSupport</a>



<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/61d0e44c-f1be-4837-a773-48c6c5278fe0">IWMDMDeviceControl::GetCapabilities</a>



<a href="https://msdn.microsoft.com/f416a520-197c-4607-979e-8f43951f2076">IWMDMDeviceControl::Seek</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a>
 

 

