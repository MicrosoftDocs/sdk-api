---
UID: NF:netcon.INetSharingConfiguration.get_EnumPortMappings
title: INetSharingConfiguration::get_EnumPortMappings (netcon.h)
description: The get_EnumPortMappings method retrieves an IEnumNetSharingPortMapping interface. Use this interface to enumerate the port mappings for this connection.
helpviewer_keywords: ["INetSharingConfiguration interface [ICS/ICF]","get_EnumPortMappings method","INetSharingConfiguration.get_EnumPortMappings","INetSharingConfiguration::get_EnumPortMappings","_ics_inetsharingconfiguration_enumportmappings","get_EnumPortMappings","get_EnumPortMappings method [ICS/ICF]","get_EnumPortMappings method [ICS/ICF]","INetSharingConfiguration interface","ics.inetsharingconfiguration_enumportmappings","netcon/INetSharingConfiguration::get_EnumPortMappings"]
old-location: ics\inetsharingconfiguration_enumportmappings.htm
tech.root: ics
ms.assetid: f5465acc-2b36-47d1-b48f-b36df3a8efb3
ms.date: 12/05/2018
ms.keywords: INetSharingConfiguration interface [ICS/ICF],get_EnumPortMappings method, INetSharingConfiguration.get_EnumPortMappings, INetSharingConfiguration::get_EnumPortMappings, _ics_inetsharingconfiguration_enumportmappings, get_EnumPortMappings, get_EnumPortMappings method [ICS/ICF], get_EnumPortMappings method [ICS/ICF],INetSharingConfiguration interface, ics.inetsharingconfiguration_enumportmappings, netcon/INetSharingConfiguration::get_EnumPortMappings
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
 - INetSharingConfiguration::get_EnumPortMappings
 - netcon/INetSharingConfiguration::get_EnumPortMappings
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
 - INetSharingConfiguration.get_EnumPortMappings
---

# INetSharingConfiguration::get_EnumPortMappings


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_EnumPortMappings</b> method retrieves an 
<a href="/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a> interface. Use this interface to enumerate the port mappings for this connection.

## -parameters

### -param Flags [in]

This parameter must be ICSSC_DEFAULT.

### -param ppColl [out]

Pointer to an interface pointer that, on successful return, points to a 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmappingcollection">INetSharingPortMappingCollection</a> interface.

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

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a particular connection.

## -see-also

<a href="/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-removeportmapping">INetSharingConfiguration::RemovePortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmappingcollection">INetSharingPortMappingCollection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>