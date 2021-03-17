---
UID: NF:netcon.INetSharingConfiguration.RemovePortMapping
title: INetSharingConfiguration::RemovePortMapping (netcon.h)
description: The RemovePortMapping method removes a service port mapping from the list of mappings for this connection.
helpviewer_keywords: ["INetSharingConfiguration interface [ICS/ICF]","RemovePortMapping method","INetSharingConfiguration.RemovePortMapping","INetSharingConfiguration::RemovePortMapping","RemovePortMapping","RemovePortMapping method [ICS/ICF]","RemovePortMapping method [ICS/ICF]","INetSharingConfiguration interface","_ics_inetsharingconfiguration_removeportmapping","ics.inetsharingconfiguration_removeportmapping","netcon/INetSharingConfiguration::RemovePortMapping"]
old-location: ics\inetsharingconfiguration_removeportmapping.htm
tech.root: ics
ms.assetid: 2790aced-a3a9-425d-9e0f-fe8df4fcb934
ms.date: 12/05/2018
ms.keywords: INetSharingConfiguration interface [ICS/ICF],RemovePortMapping method, INetSharingConfiguration.RemovePortMapping, INetSharingConfiguration::RemovePortMapping, RemovePortMapping, RemovePortMapping method [ICS/ICF], RemovePortMapping method [ICS/ICF],INetSharingConfiguration interface, _ics_inetsharingconfiguration_removeportmapping, ics.inetsharingconfiguration_removeportmapping, netcon/INetSharingConfiguration::RemovePortMapping
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
 - INetSharingConfiguration::RemovePortMapping
 - netcon/INetSharingConfiguration::RemovePortMapping
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
 - INetSharingConfiguration.RemovePortMapping
---

# INetSharingConfiguration::RemovePortMapping


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>RemovePortMapping</b> method removes a service port mapping from the list of mappings for this connection.

## -parameters

### -param pMapping [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmapping">INetSharingPortMapping</a> interface for the port mapping to remove.

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

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a particular connection.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>