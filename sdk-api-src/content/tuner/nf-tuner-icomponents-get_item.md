---
UID: NF:tuner.IComponents.get_Item
title: IComponents::get_Item method
author: windows-driver-content
description: The get_Item method enables the caller to access a component by index.
old-location: mstv\icomponents_get_item.htm
old-project: mstv
ms.assetid: 12716c7c-3156-401e-8f1c-be3100afb912
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IComponents, IComponents interface [Microsoft TV Technologies], get_Item method, IComponents::get_Item, IComponentsget_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies], IComponents interface, get_Item,IComponents.get_Item, mstv.icomponents_get_item, tuner/IComponents::get_Item
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
-	IComponents.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponents::get_Item method


## -description



The <b>get_Item</b> method enables the caller to access a component by index.




## -parameters




### -param Index [in]

Variable of type <b>VARIANT</b> specifying the zero-based index in the collection.


### -param ppComponent [out]

Address of an <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a> interface pointer that will receive the <b>Component</b> object at the specified index.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>
 

 

