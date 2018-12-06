---
UID: NF:netcon.IEnumNetSharingPortMapping.Next
title: IEnumNetSharingPortMapping::Next
author: windows-sdk-content
description: The Next method retrieves the specified number of port mappings that start from the current enumeration position.
old-location: ics\ienumnetsharingportmapping_next.htm
tech.root: ics
ms.assetid: bf90fca7-0c4f-474f-a856-7d6865ea8f03
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumNetSharingPortMapping interface [ICS/ICF],Next method, IEnumNetSharingPortMapping.Next, IEnumNetSharingPortMapping::Next, Next, Next method [ICS/ICF], Next method [ICS/ICF],IEnumNetSharingPortMapping interface, _ics_ienumnetsharingportmapping_next, ics.ienumnetsharingportmapping_next, netcon/IEnumNetSharingPortMapping::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IEnumNetSharingPortMapping::Next


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>Next</b> method retrieves the specified number of port mappings that start from the current enumeration position.


## -parameters




### -param celt [in]

Specifies the number of port mappings to retrieve.


### -param rgVar [out]

Pointer to a 
<a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> variable for the port mapping. This variant contains a pointer to an 
<a href="https://msdn.microsoft.com/236608c3-061e-4db0-96df-25d263b6463b">INetSharingPortMapping</a> interface.


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




<a href="https://msdn.microsoft.com/68334bd2-353f-457d-a2c7-1271816f10f5">IEnumNetSharingPortMapping</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

