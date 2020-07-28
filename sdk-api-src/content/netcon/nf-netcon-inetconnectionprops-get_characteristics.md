---
UID: NF:netcon.INetConnectionProps.get_Characteristics
title: INetConnectionProps::get_Characteristics (netcon.h)
description: The get_Characteristics method retrieves the media type for the connection.
helpviewer_keywords: ["INetConnectionProps interface [ICS/ICF]","get_Characteristics method","INetConnectionProps.get_Characteristics","INetConnectionProps::get_Characteristics","get_Characteristics","get_Characteristics method [ICS/ICF]","get_Characteristics method [ICS/ICF]","INetConnectionProps interface","ics.inetconnectionprops_get_characteristics","netcon/INetConnectionProps::get_Characteristics"]
old-location: ics\inetconnectionprops_get_characteristics.htm
tech.root: ics
ms.assetid: 7556fd9e-85ce-4c3a-805d-23702ca0e1c2
ms.date: 12/05/2018
ms.keywords: INetConnectionProps interface [ICS/ICF],get_Characteristics method, INetConnectionProps.get_Characteristics, INetConnectionProps::get_Characteristics, get_Characteristics, get_Characteristics method [ICS/ICF], get_Characteristics method [ICS/ICF],INetConnectionProps interface, ics.inetconnectionprops_get_characteristics, netcon/INetConnectionProps::get_Characteristics
f1_keywords:
- netcon/INetConnectionProps.get_Characteristics
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Hnetcfg.dll
api_name:
- INetConnectionProps.get_Characteristics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetConnectionProps::get_Characteristics


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_Characteristics</b> method retrieves the media type for the connection.


## -parameters




### -param pdwFlags [out]

Media types as defined by <a href="https://docs.microsoft.com/windows/desktop/api/netcon/ne-netcon-netcon_mediatype">NETCON_MEDIATYPE</a>.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnectionprops">INetConnectionProps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netcon/ne-netcon-netcon_mediatype">NETCON_MEDIATYPE</a>
 

 

