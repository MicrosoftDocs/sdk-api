---
UID: NF:netcon.INetSharingPortMappingProps.get_InternalPort
title: INetSharingPortMappingProps::get_InternalPort (netcon.h)
description: The get_InternalPort method retrieves the internal port associated with this port mapping.
helpviewer_keywords: ["INetSharingPortMappingProps interface [ICS/ICF]","get_InternalPort method","INetSharingPortMappingProps.get_InternalPort","INetSharingPortMappingProps::get_InternalPort","_ics_inetsharingportmappingprops_get_port","get_InternalPort","get_InternalPort method [ICS/ICF]","get_InternalPort method [ICS/ICF]","INetSharingPortMappingProps interface","ics.inetsharingportmappingprops_get_internalport","ics.inetsharingportmappingprops_get_port","netcon/INetSharingPortMappingProps::get_InternalPort"]
old-location: ics\inetsharingportmappingprops_get_internalport.htm
tech.root: ics
ms.assetid: 53f19eee-98da-4b90-99cd-b0bed4ec6d6f
ms.date: 12/05/2018
ms.keywords: INetSharingPortMappingProps interface [ICS/ICF],get_InternalPort method, INetSharingPortMappingProps.get_InternalPort, INetSharingPortMappingProps::get_InternalPort, _ics_inetsharingportmappingprops_get_port, get_InternalPort, get_InternalPort method [ICS/ICF], get_InternalPort method [ICS/ICF],INetSharingPortMappingProps interface, ics.inetsharingportmappingprops_get_internalport, ics.inetsharingportmappingprops_get_port, netcon/INetSharingPortMappingProps::get_InternalPort
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
 - INetSharingPortMappingProps::get_InternalPort
 - netcon/INetSharingPortMappingProps::get_InternalPort
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
 - INetSharingPortMappingProps.get_InternalPort
---

# INetSharingPortMappingProps::get_InternalPort


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_InternalPort</b> method retrieves the internal port associated with this port mapping.

## -parameters

### -param pusPort [out]

Pointer to a <b>LONG</b> variable that receives the internal port for this port mapping.

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

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmappingprops">INetSharingPortMappingProps</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>