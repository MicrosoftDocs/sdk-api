---
UID: NF:mswmdm.IWMDMDeviceControl.Pause
title: IWMDMDeviceControl::Pause (mswmdm.h)
description: The Pause method pauses the current play or record session at the current position within the content. (IWMDMDeviceControl.Pause)
helpviewer_keywords: ["IWMDMDeviceControl interface [windows Media Device Manager]","Pause method","IWMDMDeviceControl.Pause","IWMDMDeviceControl::Pause","IWMDMDeviceControlPause","Pause","Pause method [windows Media Device Manager]","Pause method [windows Media Device Manager]","IWMDMDeviceControl interface","mswmdm/IWMDMDeviceControl::Pause","wmdm.iwmdmdevicecontrol_pause"]
old-location: wmdm\iwmdmdevicecontrol_pause.htm
tech.root: WMDM
ms.assetid: 420963d1-11ea-4f1d-b5c0-749e99ee7725
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Pause method, IWMDMDeviceControl.Pause, IWMDMDeviceControl::Pause, IWMDMDeviceControlPause, Pause, Pause method [windows Media Device Manager], Pause method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Pause, wmdm.iwmdmdevicecontrol_pause
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
 - IWMDMDeviceControl::Pause
 - mswmdm/IWMDMDeviceControl::Pause
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
 - IWMDMDeviceControl.Pause
---

# IWMDMDeviceControl::Pause


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

The current playback or record session is paused and the current file position is saved. A subsequent call to the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-resume">Resume</a> method restarts the play or record operation at the saved file position.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>
