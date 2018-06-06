---
UID: NF:mswmdm.IWMDMDeviceControl.Resume
title: IWMDMDeviceControl::Resume
author: windows-sdk-content
description: The Resume method resumes the current play or record operation from the file position saved during the call to Pause.
old-location: wmdm\iwmdmdevicecontrol_resume.htm
old-project: WMDM
ms.assetid: 24ee343c-09ed-4a5f-b7be-eba15dcc4b36
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Resume method, IWMDMDeviceControl.Resume, IWMDMDeviceControl::Resume, IWMDMDeviceControlResume, Resume, Resume method [windows Media Device Manager], Resume method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Resume, wmdm.iwmdmdevicecontrol_resume
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
 - IWMDMDeviceControl.Resume
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDeviceControl::Resume


## -description



The <b>Resume</b> method resumes the current play or record operation from the file position saved during the call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>.




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
The device is not paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The resume function is not implemented on this device.

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
 




## -see-also




<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/420963d1-11ea-4f1d-b5c0-749e99ee7725">IWMDMDeviceControl::Pause</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

