---
UID: NF:msclus.ISClusProperties.CreateItem
title: ISClusProperties::CreateItem
author: windows-sdk-content
description: Creates a ClusProperty object and adds it to the ClusProperties collection.
old-location: mscs\clusproperties_createitem.htm
old-project: mscs
ms.assetid: 8df57999-5866-4005-9825-fefb827c876d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusProperties collection [Failover Cluster],CreateItem method, ClusProperties.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusProperties collection, ISClusProperties.CreateItem, ISClusProperties::CreateItem, _wolf_clusproperties.createitem, mscs.clusproperties_createitem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusProperties.CreateItem
 - ISClusProperties.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperties::CreateItem


## -description


<p class="CCE_Message">[The <b>CreateItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Creates a <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> object and adds it to the 
    <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection.


## -parameters




### -param bstrName




### -param varValue

A <b>Variant</b> specifying the initial value of the new property.


### -param pProperty






#### - strName

String. The name of the new property.


## -returns



A <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> object that 
      receives the added property.




## -remarks



The <b>CreateItem</b> method causes a 
    modification to the collection. For more information, see 
    <a href="https://msdn.microsoft.com/5eaeffda-e2ce-420a-b3f5-da8dfbfdde24">ClusProperties.Modified</a>.




## -see-also




<a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>
 

 

