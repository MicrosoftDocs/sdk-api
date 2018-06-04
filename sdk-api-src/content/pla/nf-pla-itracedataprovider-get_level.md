---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITraceDataProvider::get_Level


## -description


Retrieves the level of information used to enable the provider.

This property is read-only.


## -parameters


## -remarks



The <i>ppLevel</i> parameter is a provider-defined value that specifies the level of information that the event generates. For example, you can use this value to indicate the severity level of the events (informational, warning, error) that you want the provider to generate.

You use the <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface to retrieve or set the level value. The <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property contains the level value. 

You can also use the <a href="https://msdn.microsoft.com/4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a">IValueMap::Add</a> method to add one or more level values. You need to use the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface only when you want to name the level, or you want to enable or disable levels without having to add or remove them. Only one level can be enabled.

The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the string representation of the level, for example, Information. The <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the level value. The <a href="https://msdn.microsoft.com/f23e02bf-217a-44a2-9e1f-e92a39c1b065">IValueMapItem::Enabled</a> property indicates whether the level is enabled.  

If you use <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> to set the level and the value map collection contains one or more items, PLA searches the collection for a matching value and enables it and disables the others. If the value does not exist in the list, PLA adds the level (the item is not named).




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>
 

 

