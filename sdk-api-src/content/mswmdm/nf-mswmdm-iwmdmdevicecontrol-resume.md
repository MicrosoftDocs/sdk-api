---
UID: NF:mswmdm.IWMDMDeviceControl.Resume
title: IWMDMDeviceControl::Resume (mswmdm.h)
description: The Resume method resumes the current play or record operation from the file position saved during the call to Pause.
helpviewer_keywords: ["IWMDMDeviceControl interface [windows Media Device Manager]","Resume method","IWMDMDeviceControl.Resume","IWMDMDeviceControl::Resume","IWMDMDeviceControlResume","Resume","Resume method [windows Media Device Manager]","Resume method [windows Media Device Manager]","IWMDMDeviceControl interface","mswmdm/IWMDMDeviceControl::Resume","wmdm.iwmdmdevicecontrol_resume"]
old-location: wmdm\iwmdmdevicecontrol_resume.htm
tech.root: WMDM
ms.assetid: 24ee343c-09ed-4a5f-b7be-eba15dcc4b36
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Resume method, IWMDMDeviceControl.Resume, IWMDMDeviceControl::Resume, IWMDMDeviceControlResume, Resume, Resume method [windows Media Device Manager], Resume method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Resume, wmdm.iwmdmdevicecontrol_resume
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDeviceControl::Resume
 - mswmdm/IWMDMDeviceControl::Resume
dev_langs:
 - c++
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
---

# IWMDMDeviceControl::Resume


## -description

The <b>Resume</b> method resumes the current play or record operation from the file position saved during the call to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-pause">Pause</a>.



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

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-pause">IWMDMDeviceControl::Pause</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>
