---
UID: NF:netcon.IEnumNetSharingPortMapping.Next
title: IEnumNetSharingPortMapping::Next (netcon.h)
author: windows-sdk-content
description: The Next method retrieves the specified number of port mappings that start from the current enumeration position.
old-location: ics\ienumnetsharingportmapping_next.htm
tech.root: ics
ms.assetid: bf90fca7-0c4f-474f-a856-7d6865ea8f03
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPortMapping interface [ICS/ICF],Next method, IEnumNetSharingPortMapping.Next, IEnumNetSharingPortMapping::Next, Next, Next method [ICS/ICF], Next method [ICS/ICF],IEnumNetSharingPortMapping interface, _ics_ienumnetsharingportmapping_next, ics.ienumnetsharingportmapping_next, netcon/IEnumNetSharingPortMapping::Next
ms.topic: method
f1_keywords: ["netcon/IEnumNetSharingPortMapping.Next"]
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
 - IEnumNetSharingPortMapping.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNetSharingPortMapping::Next


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>Next</b> method retrieves the specified number of port mappings that start from the current enumeration position.


## -parameters




### -param celt [in]

Specifies the number of port mappings to retrieve.


### -param rgVar [out]

Pointer to a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a> variable for the port mapping. This variant contains a pointer to an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingportmapping">INetSharingPortMapping</a> interface.


### -param pceltFetched [out]

Pointer to a <b>ULONG</b> variable that, on successful return, specifies the number of port mappings actually returned.


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




<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

