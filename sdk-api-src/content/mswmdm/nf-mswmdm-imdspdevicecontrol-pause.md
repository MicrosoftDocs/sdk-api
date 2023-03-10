---
UID: NF:mswmdm.IMDSPDeviceControl.Pause
title: IMDSPDeviceControl::Pause (mswmdm.h)
description: The Pause method pauses the current play or record session at the current position within the content. (IMDSPDeviceControl.Pause)
helpviewer_keywords: ["IMDSPDeviceControl interface [windows Media Device Manager]","Pause method","IMDSPDeviceControl.Pause","IMDSPDeviceControl::Pause","IMDSPDeviceControlPause","Pause","Pause method [windows Media Device Manager]","Pause method [windows Media Device Manager]","IMDSPDeviceControl interface","mswmdm/IMDSPDeviceControl::Pause","wmdm.imdspdevicecontrol_pause"]
old-location: wmdm\imdspdevicecontrol_pause.htm
tech.root: WMDM
ms.assetid: d97edbd0-afac-4197-b9bc-e538c2b145b2
ms.date: 12/05/2018
ms.keywords: IMDSPDeviceControl interface [windows Media Device Manager],Pause method, IMDSPDeviceControl.Pause, IMDSPDeviceControl::Pause, IMDSPDeviceControlPause, Pause, Pause method [windows Media Device Manager], Pause method [windows Media Device Manager],IMDSPDeviceControl interface, mswmdm/IMDSPDeviceControl::Pause, wmdm.imdspdevicecontrol_pause
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
 - IMDSPDeviceControl::Pause
 - mswmdm/IMDSPDeviceControl::Pause
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
 - IMDSPDeviceControl.Pause
---

# IMDSPDeviceControl::Pause


## -description

The <b>Pause</b> method pauses the current play or record session at the current position within the content.



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

The current play or record session is paused and the current file position is saved. A subsequent call to the <b>Resume</b> method restarts the play or record operation at the saved file position.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol">IMDSPDeviceControl Interface</a>
