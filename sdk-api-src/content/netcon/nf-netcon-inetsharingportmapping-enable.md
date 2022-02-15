---
UID: NF:netcon.INetSharingPortMapping.Enable
title: INetSharingPortMapping::Enable (netcon.h)
description: The Enable method enables a port mapping for a particular connection.
helpviewer_keywords: ["Enable","Enable method [ICS/ICF]","Enable method [ICS/ICF]","INetSharingPortMapping interface","INetSharingPortMapping interface [ICS/ICF]","Enable method","INetSharingPortMapping.Enable","INetSharingPortMapping::Enable","_ics_inetsharingportmapping_enable","ics.inetsharingportmapping_enable","netcon/INetSharingPortMapping::Enable"]
old-location: ics\inetsharingportmapping_enable.htm
tech.root: ics
ms.assetid: 55a639f3-9180-4d02-9d10-659a398fa32f
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [ICS/ICF], Enable method [ICS/ICF],INetSharingPortMapping interface, INetSharingPortMapping interface [ICS/ICF],Enable method, INetSharingPortMapping.Enable, INetSharingPortMapping::Enable, _ics_inetsharingportmapping_enable, ics.inetsharingportmapping_enable, netcon/INetSharingPortMapping::Enable
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
 - INetSharingPortMapping::Enable
 - netcon/INetSharingPortMapping::Enable
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
 - INetSharingPortMapping.Enable
---

# INetSharingPortMapping::Enable


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The <b>Enable</b> method enables a port mapping for a particular connection.



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

## -remarks

Calling this method puts a check mark in the box next to this port mapping in the ICS/ICF user interface.

When first added, a new mapping is in a disabled state. Use the  
<b>Enable</b> method to enable the new mapping.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmapping">INetSharingPortMapping</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
