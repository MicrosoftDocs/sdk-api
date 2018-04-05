---
UID: NF:tuner.IComponentTypes.get_Item
title: IComponentTypes::get_Item method
author: windows-driver-content
description: The get_Item method retrieves the IComponentType interface pointer at the specified index number.
old-location: mstv\icomponenttypes_get_item.htm
old-project: mstv
ms.assetid: be2e6f1b-a9af-4c19-ae25-a096ceee96fc
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IComponentTypes, IComponentTypes interface [Microsoft TV Technologies], get_Item method, IComponentTypes::get_Item, IComponentTypesget_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies], IComponentTypes interface, get_Item,IComponentTypes.get_Item, mstv.icomponenttypes_get_item, tuner/IComponentTypes::get_Item
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
-	IComponentTypes.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentTypes::get_Item method


## -description



The <b>get_Item</b> method retrieves the <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface pointer at the specified index number.




## -parameters




### -param Index [in]

The index number of the object to retrieve.


### -param ComponentType






#### - ppComponentType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes Interface</a>
 

 

