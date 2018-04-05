---
UID: NF:tuner.IComponent.Clone
title: IComponent::Clone method
author: windows-driver-content
description: The Clone method creates a copy of the component.
old-location: mstv\icomponent_clone.htm
old-project: mstv
ms.assetid: 8d643a76-c0aa-4ded-9534-0ff7c4e8402d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies], IComponent interface, Clone,IComponent.Clone, IComponent, IComponent interface [Microsoft TV Technologies], Clone method, IComponent::Clone, IComponentClone, mstv.icomponent_clone, tuner/IComponent::Clone
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
-	IComponent.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponent::Clone method


## -description



The <b>Clone</b> method creates a copy of the component.




## -parameters




### -param NewComponent






#### - ppNewComponent [out]

Receives an <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a> interface pointer. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

