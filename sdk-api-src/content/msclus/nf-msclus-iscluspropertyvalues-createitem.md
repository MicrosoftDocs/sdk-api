---
UID: NF:msclus.ISClusPropertyValues.CreateItem
title: ISClusPropertyValues::CreateItem
author: windows-sdk-content
description: Creates a property value and adds it to the ClusPropertyValues collection.
old-location: mscs\cluspropertyvalues_createitem.htm
old-project: mscs
ms.assetid: b7175a46-3e0c-4d71-b435-589a145a56f3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusPropertyValues collection [Failover Cluster],CreateItem method, ClusPropertyValues.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusPropertyValues collection, ISClusPropertyValues.CreateItem, ISClusPropertyValues::CreateItem, _wolf_cluspropertyvalues.createitem, mscs.cluspropertyvalues_createitem
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
 - ClusPropertyValues.CreateItem
 - ISClusPropertyValues.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusPropertyValues::CreateItem


## -description


<p class="CCE_Message">[The <b>CreateItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Creates 
    a <a href="p_gly.htm">property value</a> and adds it to the 
    <a href="https://msdn.microsoft.com/18ae71ee-5582-4ac9-bb0f-f1c077c0352a">ClusPropertyValues</a> 
    collection.


## -parameters




### -param bstrName




### -param varValue

A <b>Variant</b> specifying the new property value.


### -param ppPropertyValue






#### - strName

A <b>String</b> containing the name of the property to which this value 
      applies.


## -returns



A <a href="https://msdn.microsoft.com/6a8ffae6-c4f3-42fb-9703-eeb695902877">ClusPropertyValue</a> object that receives 
      the new property value.




## -see-also




<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>



<a href="https://msdn.microsoft.com/18ae71ee-5582-4ac9-bb0f-f1c077c0352a">ClusPropertyValues</a>
 

 

