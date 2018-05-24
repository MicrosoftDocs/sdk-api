---
UID: NF:pla.IFolderActionCollection.get__NewEnum
title: IFolderActionCollection::get__NewEnum
author: windows-driver-content
description: Retrieves an interface to the enumeration.
old-location: pla\ifolderactioncollection__newenum.htm
old-project: PLA
ms.assetid: 92b13b4f-31bd-42c7-9aed-02cef9ca38f3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IFolderActionCollection interface [PLA],_NewEnum property, IFolderActionCollection._NewEnum, IFolderActionCollection.get__NewEnum, IFolderActionCollection::_NewEnum, IFolderActionCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IFolderActionCollection interface, base.ifolderactioncollection__newenum, get__NewEnum, pla.ifolderactioncollection__newenum, pla/IFolderActionCollection::_NewEnum, pla/IFolderActionCollection::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IFolderActionCollection._NewEnum
-	IFolderActionCollection.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFolderActionCollection::get__NewEnum


## -description


Retrieves an interface to the enumeration.

This property is read-only.


## -parameters


## -remarks



C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="https://msdn.microsoft.com/a3942d5f-9ec4-4461-84f9-f2fae3971e23">IFolderAction</a> interface, use the <b>punkVal</b> member of the variant.




## -see-also




<a href="https://msdn.microsoft.com/9b0ab26f-7e91-4d7a-9fd7-73332601dd7b">IFolderActionCollection</a>
 

 

