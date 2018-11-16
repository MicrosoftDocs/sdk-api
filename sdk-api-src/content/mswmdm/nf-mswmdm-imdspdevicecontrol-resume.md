---
UID: NF:mswmdm.IMDSPDeviceControl.Resume
title: IMDSPDeviceControl::Resume
author: windows-sdk-content
description: The Resume method resumes the current playback or record operation from the file position saved during the call to Pause.
old-location: wmdm\imdspdevicecontrol_resume.htm
tech.root: WMDM
ms.assetid: 6c7e26dc-05cd-4dfd-86c8-0b7b216b6772
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMDSPDeviceControl interface [windows Media Device Manager],Resume method, IMDSPDeviceControl.Resume, IMDSPDeviceControl::Resume, IMDSPDeviceControlResume, Resume, Resume method [windows Media Device Manager], Resume method [windows Media Device Manager],IMDSPDeviceControl interface, mswmdm/IMDSPDeviceControl::Resume, wmdm.imdspdevicecontrol_resume
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
 - IMDSPDeviceControl.Resume
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
- IMDSPDeviceControl.Resume
: 
---

# IMDSPDeviceControl::Resume


## -description



The <b>Resume</b> method resumes the current playback or record operation from the file position saved during the call to <a href="https://msdn.microsoft.com/d97edbd0-afac-4197-b9bc-e538c2b145b2">Pause</a>.




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




<a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/d97edbd0-afac-4197-b9bc-e538c2b145b2">IMDSPDeviceControl::Pause</a>
 

 

