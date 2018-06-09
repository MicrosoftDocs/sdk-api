---
UID: NF:msclus.ISClusResource.get_TypeName
title: ISClusResource::get_TypeName
author: windows-sdk-content
description: Returns the resource type name of the resource.
old-location: mscs\clusresource_typename.htm
old-project: MsCS
ms.assetid: a3230fa1-67f9-43d5-b06a-03ffc2487a63
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusResource class [Failover Cluster],TypeName property, ClusResource.TypeName, ISClusResource.get_TypeName, ISClusResource::get_TypeName, TypeName property [Failover Cluster], TypeName property [Failover Cluster],ClusResource class, _wolf_clusresource.typename, get_TypeName, mscs.clusresource_typename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusResource.TypeName
 - ISClusResource.get_TypeName
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::get_TypeName


## -description


<p class="CCE_Message">[The <b>TypeName</b> property 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Returns the 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> name of the 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.

This property is read-only.


## -parameters


## -remarks



The name returned is the name of the resource type as registered with the 
    <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>, for example: 
    "<a href="https://msdn.microsoft.com/414c5f97-0a3a-4e01-8ab7-340f547ba101">File Share</a>" or 
    "<a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a>".




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/1393df7b-7ec7-4034-8018-d7f5b7cef3e8">ClusResource.Type</a>
 

 

