---
UID: NF:netcon.INetSharingPortMappingProps.get_IPProtocol
title: INetSharingPortMappingProps::get_IPProtocol
author: windows-sdk-content
description: The get_IPProtocol method retrieves the IP Protocol associated with this port mapping.
old-location: ics\inetsharingportmappingprops_get_ipprotocol.htm
tech.root: ics
ms.assetid: a227074e-014b-4b76-b1d7-e1728bd99270
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: INetSharingPortMappingProps interface [ICS/ICF],get_IPProtocol method, INetSharingPortMappingProps.get_IPProtocol, INetSharingPortMappingProps::get_IPProtocol, _ics_inetsharingportmappingprops_get_ipprotocol, get_IPProtocol, get_IPProtocol method [ICS/ICF], get_IPProtocol method [ICS/ICF],INetSharingPortMappingProps interface, ics.inetsharingportmappingprops_get_ipprotocol, netcon/INetSharingPortMappingProps::get_IPProtocol
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
 - INetSharingPortMappingProps.get_IPProtocol
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingPortMappingProps::get_IPProtocol


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>get_IPProtocol</b> method retrieves the IP Protocol associated with this port mapping.


## -parameters




### -param pucIPProt [out]

Pointer to a <b>UCHAR</b> variable that receives the IP Protocol for the port mapping. The IP Protocol is one of the following values: 




NAT_PROTOCOL_TCP

NAT_PROTOCOL_UDP


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




<a href="https://msdn.microsoft.com/9fa20653-5224-4588-89fb-8d4ce07b4235">INetSharingPortMappingProps</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

