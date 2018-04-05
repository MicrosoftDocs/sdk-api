---
UID: NF:tuner.IComponentTypes.put_Item
title: IComponentTypes::put_Item method
author: windows-driver-content
description: The put_Item method replaces the ComponentType object at the specified index with a new ComponentType object.
old-location: mstv\icomponenttypes_put_item.htm
old-project: mstv
ms.assetid: 1f38e844-d197-40c1-8715-ffe406274b3c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IComponentTypes, IComponentTypes interface [Microsoft TV Technologies], put_Item method, IComponentTypes::put_Item, IComponentTypesput_Item, mstv.icomponenttypes_put_item, put_Item method [Microsoft TV Technologies], put_Item method [Microsoft TV Technologies], IComponentTypes interface, put_Item,IComponentTypes.put_Item, tuner/IComponentTypes::put_Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponentTypes.put_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentTypes::put_Item method


## -description



The <b>put_Item</b> method replaces the <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> object at the specified index with a new <b>ComponentType</b> object.




## -parameters




### -param Index [in]

Index number of the item to be replaced.


### -param ComponentType






#### - pComponentType [in]

Pointer to the <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> object that will be inserted into the collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes Interface</a>
 

 

