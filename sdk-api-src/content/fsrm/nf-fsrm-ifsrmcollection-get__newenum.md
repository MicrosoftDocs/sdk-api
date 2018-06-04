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

# IFsrmCollection::get__NewEnum


## -description


Retrieves the <a href="_com_IUnknown">IUnknown</a> pointer of a new 
    <a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> enumeration for the items in 
    the collection.

This property is read-only.


## -parameters


## -remarks



C/C++ users use this method to enumerate items in the collection. Call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> of the 
    <a href="_com_IUnknown">IUnknown</a> interface to get the 
    <a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface. Use the 
    <a href="https://msdn.microsoft.com/691c1624-8d01-41e0-890e-a4782eba1f59">IEnumVARIANT::Next</a> method to enumerate 
    the items of the collection. The items are returned as <b>VARIANT</b> values.

If the collection contains interfaces, the  variant type is <b>VT_DISPATCH</b>. Call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the 
    <b>pdispVal</b> member of the variant to get an interface to the specific object. For example, 
    if the collection contains report objects, you would query the <b>pdispVal</b> member for the 
    <a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a> interface.

If the item is an <b>HRESULT</b> value, the variant type is 
    <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to get the 
    <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

