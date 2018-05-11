---
UID: NF:tuner.IComponent.get_Description
title: IComponent::get_Description
author: windows-driver-content
description: The get_Description method retrieves the description of the component.
old-location: mstv\icomponent_get_description.htm
old-project: mstv
ms.assetid: ef7d1308-27ff-4d4d-b88d-58a9f89abc7f
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_Description method, IComponent.get_Description, IComponent::get_Description, IComponentget_Description, get_Description, get_Description method [Microsoft TV Technologies], get_Description method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_description, tuner/IComponent::get_Description
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
-	IComponent.get_Description
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponent::get_Description


## -description



The <b>get_Description</b> method retrieves the description of the component.




## -parameters




### -param Description






#### - pDescription [out]

Pointer to a variable that receives the description.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

