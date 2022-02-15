---
UID: NF:mswmdm.IWMDMDeviceControl.Stop
title: IWMDMDeviceControl::Stop (mswmdm.h)
description: The Stop method stops the current record or play operation.
helpviewer_keywords: ["IWMDMDeviceControl interface [windows Media Device Manager]","Stop method","IWMDMDeviceControl.Stop","IWMDMDeviceControl::Stop","IWMDMDeviceControlStop","Stop","Stop method [windows Media Device Manager]","Stop method [windows Media Device Manager]","IWMDMDeviceControl interface","mswmdm/IWMDMDeviceControl::Stop","wmdm.iwmdmdevicecontrol_stop"]
old-location: wmdm\iwmdmdevicecontrol_stop.htm
tech.root: WMDM
ms.assetid: 842b7de7-dde2-40d1-8028-9ffebcaea90e
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Stop method, IWMDMDeviceControl.Stop, IWMDMDeviceControl::Stop, IWMDMDeviceControlStop, Stop, Stop method [windows Media Device Manager], Stop method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Stop, wmdm.iwmdmdevicecontrol_stop
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
 - IWMDMDeviceControl::Stop
 - mswmdm/IWMDMDeviceControl::Stop
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
 - IWMDMDeviceControl.Stop
---

# IWMDMDeviceControl::Stop


## -description

The <b>Stop</b> method stops the current record or play operation.



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
The device is busy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The stop function is not implemented on this device.

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



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo Interface</a>
