---
UID: NN:netcon.INetSharingPortMappingProps
title: INetSharingPortMappingProps
author: windows-sdk-content
description: The INetSharingPortMappingProps interface provides methods that retrieve and set the properties of a network connection port mapping.
old-location: ics\inetsharingportmappingprops.htm
old-project: ICS
ms.assetid: 9fa20653-5224-4588-89fb-8d4ce07b4235
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: INetSharingPortMappingProps, INetSharingPortMappingProps interface [ICS/ICF], INetSharingPortMappingProps interface [ICS/ICF],described, _ics_inetsharingportmappingprops, ics.inetsharingportmappingprops, netcon/INetSharingPortMappingProps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingPortMappingProps
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingPortMappingProps interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingPortMappingProps</b> interface provides methods that retrieve and set the properties of a network connection port mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPortMappingProps</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetSharingPortMappingProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPortMappingProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad8c20d5-e9af-4c9d-af05-69decd24dae2">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieve the port mapping status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1cf6a3f-c6d2-4514-89e6-af58be22dabb">get_ExternalPort</a>
</td>
<td align="left" width="63%">
Retrieve the  external port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53f19eee-98da-4b90-99cd-b0bed4ec6d6f">get_InternalPort</a>
</td>
<td align="left" width="63%">
Retrieve the internal port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a227074e-014b-4b76-b1d7-e1728bd99270">get_IPProtocol</a>
</td>
<td align="left" width="63%">
Retrieve the IP protocol associated with this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f2b4d49-a13d-49e1-96d0-276afe4208b2">get_Name</a>
</td>
<td align="left" width="63%">
Retrieve the name for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4df3258d-27d8-41b3-a58b-655d643929f5">get_Options</a>
</td>
<td align="left" width="63%">
Retrieve the options for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af794535-8b36-4306-a220-f4938f0e6ee9">get_TargetIPAddress</a>
</td>
<td align="left" width="63%">
Retrieve the target IP address for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc486e8d-a927-4e38-9fcd-ab4410270cad">get_TargetName</a>
</td>
<td align="left" width="63%">
Retrieve the target name for this port mapping.

</td>
</tr>
</table> 

