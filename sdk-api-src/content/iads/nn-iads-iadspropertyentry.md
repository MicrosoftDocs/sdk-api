---
UID: NN:iads.IADsPropertyEntry
title: IADsPropertyEntry (iads.h)
author: windows-sdk-content
description: The IADsPropertyEntry interface is used to manage a property entry in the property cache.
old-location: adsi\iadspropertyentry.htm
tech.root: adsi
ms.assetid: 6c398d05-ac12-4c9a-b61a-70cd795c991f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsPropertyEntry, IADsPropertyEntry interface [ADSI], IADsPropertyEntry interface [ADSI],described, PropertyEntry, _ds_iadspropertyentry, adsi.iadspropertyentry, iads/IADsPropertyEntry
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPropertyEntry
 - PropertyEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsPropertyEntry interface


## -description


The <b>IADsPropertyEntry</b> interface is used to manage a property entry in the 
property cache. A property entry holds a value (or values) of an attribute as defined in the schema. It is identified by the name of the corresponding attribute. A property entry object allows a user to specify how its values are to be manipulated. Examples of such operations include "update,"
    "modify," and "delete".

Multiple property entries are managed by a property list. To access a property entry, you call  <a href="https://msdn.microsoft.com/6e103872-ea2e-4178-9c8a-b958ae3bcf85">Item</a> or  <a href="https://msdn.microsoft.com/1de86caa-c14c-4dc0-bf56-5fa33279e30a">GetPropertyItem</a> method on the  <a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a> interface.

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



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

