---
UID: NF:netcon.INetConnectionProps.get_Guid
title: INetConnectionProps::get_Guid (netcon.h)
description: The get_Guid method retrieves the globally-unique identifier (GUID) for the connection.
helpviewer_keywords: ["INetConnectionProps interface [ICS/ICF]","get_Guid method","INetConnectionProps.get_Guid","INetConnectionProps::get_Guid","_ics_inetconnectionprops_get_guid","get_Guid","get_Guid method [ICS/ICF]","get_Guid method [ICS/ICF]","INetConnectionProps interface","ics.inetconnectionprops_get_guid","netcon/INetConnectionProps::get_Guid"]
old-location: ics\inetconnectionprops_get_guid.htm
tech.root: ics
ms.assetid: df094bda-2e0f-4ff4-aff5-77d1703f8dee
ms.date: 12/05/2018
ms.keywords: INetConnectionProps interface [ICS/ICF],get_Guid method, INetConnectionProps.get_Guid, INetConnectionProps::get_Guid, _ics_inetconnectionprops_get_guid, get_Guid, get_Guid method [ICS/ICF], get_Guid method [ICS/ICF],INetConnectionProps interface, ics.inetconnectionprops_get_guid, netcon/INetConnectionProps::get_Guid
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
 - INetConnectionProps::get_Guid
 - netcon/INetConnectionProps::get_Guid
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
 - INetConnectionProps.get_Guid
---

# INetConnectionProps::get_Guid


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_Guid</b> method retrieves the globally-unique identifier (GUID) for the connection.

## -parameters

### -param pbstrGuid [out]

Pointer to a 
<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> variable that, on successful return, receives the GUID for the connection.

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