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

# IFsrmCollection::get_Item


## -description


Retrieves the requested item from the collection.

This property is read-only.


## -parameters


## -remarks



If the item is an interface, the variant type is <b>VT_DISPATCH</b>. Call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the 
    <b>pdispVal</b> member of the variant to get an interface to the specific object.

If the item is an <b>HRESULT</b> value, the variant type is 
    <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to get the 
    <b>HRESULT</b> value.


#### Examples

For examples, see 
     <a href="https://msdn.microsoft.com/298e7e37-709a-4b13-87d3-605d540d8f85">Updating a File Screen</a> and 
     <a href="https://msdn.microsoft.com/94e382d6-3e18-4c80-aed2-4c2d58699236">Classifying Files</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

