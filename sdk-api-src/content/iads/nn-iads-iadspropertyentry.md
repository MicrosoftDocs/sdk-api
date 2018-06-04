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

# IADsPropertyEntry interface


## -description


The <b>IADsPropertyEntry</b> interface is used to manage a property entry in the 
property cache. A property entry holds a value (or values) of an attribute as defined in the schema. It is identified by the name of the corresponding attribute. A property entry object allows a user to specify how its values are to be manipulated. Examples of such operations include "update,"
    "modify," and "delete".

Multiple property entries are managed by a property list. To access a property entry, you call  <a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> or  <a href="https://msdn.microsoft.com/1de86caa-c14c-4dc0-bf56-5fa33279e30a">GetPropertyItem</a> method on the  <a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a> interface.

Use the property methods of <b>IADsPropertyEntry</b> to examine and manipulate individual properties. Before calling the methods of this interface, you must call  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> or  <a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a> explicitly to load the assigned property values of the object into the cache. After calling the methods of this interfaces, you must call  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> to save the changes in the persistent store of the underlying directory.


## -see-also




<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/73b0f6d4-55db-46cf-a781-e10bc4fcf2db">IADsPropertyEntry
    Property Methods</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/1de86caa-c14c-4dc0-bf56-5fa33279e30a">IADsPropertyList::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/6e103872-ea2e-4178-9c8a-b958ae3bcf85">IADsPropertyList::Item</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

