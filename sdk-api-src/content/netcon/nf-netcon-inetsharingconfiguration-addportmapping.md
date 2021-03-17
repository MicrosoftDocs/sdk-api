---
UID: NF:netcon.INetSharingConfiguration.AddPortMapping
title: INetSharingConfiguration::AddPortMapping (netcon.h)
description: Adds a service port mapping for this connection.
helpviewer_keywords: ["AddPortMapping","AddPortMapping method [ICS/ICF]","AddPortMapping method [ICS/ICF]","INetSharingConfiguration interface","INetSharingConfiguration interface [ICS/ICF]","AddPortMapping method","INetSharingConfiguration.AddPortMapping","INetSharingConfiguration::AddPortMapping","_ics_inetsharingconfiguration_addportmapping","ics.inetsharingconfiguration_addportmapping","netcon/INetSharingConfiguration::AddPortMapping"]
old-location: ics\inetsharingconfiguration_addportmapping.htm
tech.root: ics
ms.assetid: 0d9e1520-6018-425c-a2f9-c408fa3025cf
ms.date: 12/05/2018
ms.keywords: AddPortMapping, AddPortMapping method [ICS/ICF], AddPortMapping method [ICS/ICF],INetSharingConfiguration interface, INetSharingConfiguration interface [ICS/ICF],AddPortMapping method, INetSharingConfiguration.AddPortMapping, INetSharingConfiguration::AddPortMapping, _ics_inetsharingconfiguration_addportmapping, ics.inetsharingconfiguration_addportmapping, netcon/INetSharingConfiguration::AddPortMapping
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
 - INetSharingConfiguration::AddPortMapping
 - netcon/INetSharingConfiguration::AddPortMapping
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
 - INetSharingConfiguration.AddPortMapping
---

# INetSharingConfiguration::AddPortMapping


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>AddPortMapping</b> method adds a service port mapping for this connection.

## -parameters

### -param bstrName [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> variable that contains the name for this port mapping.

### -param ucIPProtocol [in]

Specifies the IP Protocol to set for the port mapping. The IP Protocol is one of the following values: 




NAT_PROTOCOL_TCP

NAT_PROTOCOL_UDP

### -param usExternalPort [in]

Specifies the external port for this port mapping.

### -param usInternalPort [in]

Specifies the internal port for this port mapping.

### -param dwOptions [in]

This parameter is reserved and not used at this time.

### -param bstrTargetNameOrIPAddress [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> variable that contains the name of the target computer for this port mapping. Specify either the target name or the target IP address, but not both.

### -param eTargetType [in]

Indicates target type.

### -param ppMapping [out]

Pointer to a pointer that, on successful return, points to an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmapping">INetSharingPortMapping</a> interface for the port mapping.

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

When first added, the new mapping is in a disabled state. To enable the new mapping, use 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmapping-enable">INetSharingPortMapping::Enable</a>.

After it is added, the new definition appears in the Port Mappings list in the ICS/ICF user interface.

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a particular connection.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>