---
UID: NN:gpmgmt.IGPMDomain2
title: IGPMDomain2
author: windows-sdk-content
description: Represents a given domain and supports methods that allow you to query scope of management (SOM) objects, create, restore and query Starter GPOs, and create and query WMI filters when you are using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmdomain2.htm
old-project: GPMC
ms.assetid: 5abfea14-0cb9-46ea-915c-93a8d8b2477b
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IGPMDomain2, IGPMDomain2 interface [GPMC], IGPMDomain2 interface [GPMC],described, gpmc.igpmdomain2, gpmgmt/IGPMDomain2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMDomain2
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMDomain2 interface


## -description


The 
<b>IGPMDomain2</b> interface represents a specified domain and supports certain methods.

These methods allow you to perform the following tasks when you are using the Group Policy Management Console (GPMC) interfaces:
<ul>
<li>Query scope of management (SOM) objects</li>
<li>Create, restore, and query Starter Group Policy objects (GPOs)</li>
<li>Create and query Windows Management Instrumentation (WMI) filters</li>
</ul>To create a <a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">GPMDomain</a> object, call the 
<a href="https://msdn.microsoft.com/32aee72f-96fa-4ebd-9ff7-643972b82cf6">IGPM::GetDomain</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMDomain2</b> interface inherits from <a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>. <b>IGPMDomain2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPMDomain2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a74f763-a9f5-4e93-94fb-7ef2a116c82b">CreateGPOFromStarterGPO</a>
</td>
<td align="left" width="63%">
Creates and retrieves a 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object from a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/652ac85b-f488-4e27-81dd-1ffc5f9f42d6">CreateStarterGPO</a>
</td>
<td align="left" width="63%">
Creates and retrieves a 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0648c653-94da-40d6-98c2-46f80a51bc90">GetStarterGPO</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object that has the specified GPO ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3375ecaf-6128-4bc0-9cfc-e9b00bf4b70a">LoadStarterGPO</a>
</td>
<td align="left" width="63%">
Opens a Starter GPO cabinet (CAB) file and imports it into the domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e91a3540-7f1b-4843-9b5e-4dcd837dc0f8">RestoreStarterGPO</a>
</td>
<td align="left" width="63%">
Restores the Starter GPO from a 
<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> object into the current domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30a325e8-372a-4e30-a420-10f5b6ef295d">SearchStarterGPOs</a>
</td>
<td align="left" width="63%">
Executes a search for 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> objects  in the domain and returns a 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMStarterGPOCollection</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f9cd432a-3974-4fc4-9e32-1d8e2df1601c">IGPM2</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>



<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">IGPMStarterGPOBackup</a>



<a href="https://msdn.microsoft.com/b650b1c6-0597-468a-afdc-a21d61f1a8a0">IGPMStarterGPOCollection</a>
 

 

