---
UID: NF:netcon.INetSharingPortMapping.Delete
title: INetSharingPortMapping::Delete (netcon.h)
description: The Delete method deletes a port mapping from the list of port mappings for a particular connection.
helpviewer_keywords: ["Delete","Delete method [ICS/ICF]","Delete method [ICS/ICF]","INetSharingPortMapping interface","INetSharingPortMapping interface [ICS/ICF]","Delete method","INetSharingPortMapping.Delete","INetSharingPortMapping::Delete","_ics_inetsharingportmapping_delete","ics.inetsharingportmapping_delete","netcon/INetSharingPortMapping::Delete"]
old-location: ics\inetsharingportmapping_delete.htm
tech.root: ics
ms.assetid: f9582110-a717-41a4-8ddd-26ef703b8356
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [ICS/ICF], Delete method [ICS/ICF],INetSharingPortMapping interface, INetSharingPortMapping interface [ICS/ICF],Delete method, INetSharingPortMapping.Delete, INetSharingPortMapping::Delete, _ics_inetsharingportmapping_delete, ics.inetsharingportmapping_delete, netcon/INetSharingPortMapping::Delete
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
 - INetSharingPortMapping::Delete
 - netcon/INetSharingPortMapping::Delete
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
 - INetSharingPortMapping.Delete
---

# INetSharingPortMapping::Delete


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>Delete</b> method deletes a port mapping from the list of port mappings for a particular connection.



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

Calling this method also removes the name of this port mapping from the list of mappings in the ICS/ICF user interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-removeportmapping">INetSharingConfiguration::RemovePortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmapping">INetSharingPortMapping</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
