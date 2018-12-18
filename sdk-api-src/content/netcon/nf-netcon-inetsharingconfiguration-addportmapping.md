---
UID: NF:netcon.INetSharingConfiguration.AddPortMapping
title: INetSharingConfiguration::AddPortMapping
author: windows-sdk-content
description: Adds a service port mapping for this connection.
old-location: ics\inetsharingconfiguration_addportmapping.htm
tech.root: ics
ms.assetid: 0d9e1520-6018-425c-a2f9-c408fa3025cf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddPortMapping, AddPortMapping method [ICS/ICF], AddPortMapping method [ICS/ICF],INetSharingConfiguration interface, INetSharingConfiguration interface [ICS/ICF],AddPortMapping method, INetSharingConfiguration.AddPortMapping, INetSharingConfiguration::AddPortMapping, _ics_inetsharingconfiguration_addportmapping, ics.inetsharingconfiguration_addportmapping, netcon/INetSharingConfiguration::AddPortMapping
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
 - INetSharingConfiguration.AddPortMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingConfiguration::AddPortMapping


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>AddPortMapping</b> method adds a service port mapping for this connection.


## -parameters




### -param bstrName [in]

Pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> variable that contains the name for this port mapping.


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
<a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> variable that contains the name of the target computer for this port mapping. Specify either the target name or the target IP address, but not both.


### -param eTargetType [in]

Indicates target type.


### -param ppMapping [out]

Pointer to a pointer that, on successful return, points to an 
<a href="https://msdn.microsoft.com/236608c3-061e-4db0-96df-25d263b6463b">INetSharingPortMapping</a> interface for the port mapping.


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
<a href="https://msdn.microsoft.com/55a639f3-9180-4d02-9d10-659a398fa32f">INetSharingPortMapping::Enable</a>.

After it is added, the new definition appears in the Port Mappings list in the ICS/ICF user interface.

Use the 
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface for a particular connection.




## -see-also




<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

