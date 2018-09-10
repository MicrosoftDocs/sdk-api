---
UID: NF:tuner.IComponents.put_Item
title: IComponents::put_Item
author: windows-sdk-content
description: The put_Item method inserts a component into the collection, replacing the item that is identified by the specified index.
old-location: mstv\icomponents_put_item.htm
tech.root: mstv
ms.assetid: c1e18e97-e8d3-441c-b7ea-6743e478033b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],put_Item method, IComponents.put_Item, IComponents::put_Item, IComponentsput_Item, mstv.icomponents_put_item, put_Item, put_Item method [Microsoft TV Technologies], put_Item method [Microsoft TV Technologies],IComponents interface, tuner/IComponents::put_Item
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponents.put_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponents::put_Item


## -description



The <b>put_Item</b> method inserts a component into the collection, replacing the item that is identified by the specified index.




## -parameters




### -param Index [in]

Specifies the index to assign to the component. This parameter is a value of type <b>VARIANT</b>.


### -param ppComponent

TBD




#### - pComponent [in]

Pointer to the <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a> interface of the component object. The method creates a clone of the component and inserts the clone into the collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method allows the client to replace an existing item in the collection.

If the collection contains <i>n</i> items, valid indexes are in the range 0 to <i>n</i>-1. To determine the number of items in the collection, call <a href="https://msdn.microsoft.com/ba198e27-c699-4c93-aa2d-b8be8c40380c">get_Count</a>.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>



<a href="https://msdn.microsoft.com/12716c7c-3156-401e-8f1c-be3100afb912">get_Item</a>
 

 

