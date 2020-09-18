---
UID: NF:netcon.INetConnectionProps.get_DeviceName
title: INetConnectionProps::get_DeviceName (netcon.h)
description: The get_DeviceName method retrieves the name of the device associated with the connection.
helpviewer_keywords: ["INetConnectionProps interface [ICS/ICF]","get_DeviceName method","INetConnectionProps.get_DeviceName","INetConnectionProps::get_DeviceName","_ics_inetconnectionprops_get_devicename","get_DeviceName","get_DeviceName method [ICS/ICF]","get_DeviceName method [ICS/ICF]","INetConnectionProps interface","ics.inetconnectionprops_get_devicename","netcon/INetConnectionProps::get_DeviceName"]
old-location: ics\inetconnectionprops_get_devicename.htm
tech.root: ics
ms.assetid: 4c24c5a6-d856-4c62-a98e-33e4fc216f83
ms.date: 12/05/2018
ms.keywords: INetConnectionProps interface [ICS/ICF],get_DeviceName method, INetConnectionProps.get_DeviceName, INetConnectionProps::get_DeviceName, _ics_inetconnectionprops_get_devicename, get_DeviceName, get_DeviceName method [ICS/ICF], get_DeviceName method [ICS/ICF],INetConnectionProps interface, ics.inetconnectionprops_get_devicename, netcon/INetConnectionProps::get_DeviceName
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetConnectionProps::get_DeviceName
 - netcon/INetConnectionProps::get_DeviceName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetConnectionProps.get_DeviceName
---

# INetConnectionProps::get_DeviceName


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_DeviceName</b> method retrieves the name of the device associated with the connection.

## -parameters

### -param pbstrDeviceName [out]

Pointer to a 
<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> variable that, on successful return, receives the name of the device associated with the connection.

## -returns

If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnectionprops">INetConnectionProps</a>