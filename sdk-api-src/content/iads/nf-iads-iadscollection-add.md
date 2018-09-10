---
UID: NF:iads.IADsCollection.Add
title: IADsCollection::Add
author: windows-sdk-content
description: Adds a named item to the collection.
old-location: adsi\iadscollection_add.htm
tech.root: ADSI
ms.assetid: c4f0dc3e-238c-4fd3-adb7-9d467efc8c3d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Add, Add method [ADSI], Add method [ADSI],IADsCollection interface, IADsCollection interface [ADSI],Add method, IADsCollection.Add, IADsCollection::Add, _ds_iadscollection_add, adsi.iadscollection__add, adsi.iadscollection_add, iads/IADsCollection::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IADsCollection.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsCollection::Add


## -description


The <b>IADsCollection::Add</b> method adds a named item to the collection.


## -parameters




### -param bstrName [in]

The <b>BSTR</b> value that specifies the item name.  <a href="https://msdn.microsoft.com/04b33451-505e-43de-8db4-3e37f9909ea6">IADsCollection::GetObject</a> and  <a href="https://msdn.microsoft.com/21ce80fe-542b-4350-b66c-fa26f62ca611">IADsCollection::Remove</a> reference the item by this name.


### -param vItem

TBD




#### - varItem [in]

Item value. When the item is an object, this parameter holds the  <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer on the object.


## -returns



This method supports the standard return values, as well as the following.
      

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Collections for a directory service can also consist of a set of immutable objects.

This method is not supported in any of the  <a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI system providers</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI System
  Providers</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/04b33451-505e-43de-8db4-3e37f9909ea6">IADsCollection::GetObject</a>



<a href="https://msdn.microsoft.com/21ce80fe-542b-4350-b66c-fa26f62ca611">IADsCollection::Remove</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

