---
UID: NF:tuner.IComponent.get_Type
title: IComponent::get_Type
author: windows-driver-content
description: The get_Type method retrieves an IComponentType interface describing the general characteristics of the component.
old-location: mstv\icomponent_get_type.htm
old-project: mstv
ms.assetid: 19eb345f-24a2-4522-87cc-fc4953faf343
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_Type method, IComponent.get_Type, IComponent::get_Type, IComponentget_Type, get_Type, get_Type method [Microsoft TV Technologies], get_Type method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_type, tuner/IComponent::get_Type
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
-	IComponent.get_Type
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponent::get_Type


## -description



The <b>get_Type</b> method retrieves an <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface describing the general characteristics of the component.




## -parameters




### -param CT






#### - ppCT [out]

Address of an <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface pointer that will be set to the retrieved component.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

