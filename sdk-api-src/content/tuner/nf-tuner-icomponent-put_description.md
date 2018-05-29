---
UID: NF:tuner.IComponent.put_Description
title: IComponent::put_Description
author: windows-sdk-content
description: The put_Description method sets the description of the component.
old-location: mstv\icomponent_put_description.htm
old-project: mstv
ms.assetid: e45ea3ea-e9e2-41f9-b171-bc95aa5cc590
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_Description method, IComponent.put_Description, IComponent::put_Description, IComponentput_Description, mstv.icomponent_put_description, put_Description, put_Description method [Microsoft TV Technologies], put_Description method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_Description
ms.prod: windows
ms.technology: windows-sdk
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
-	IComponent.put_Description
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponent::put_Description


## -description



The <b>put_Description</b> method sets the description of the component.




## -parameters




### -param Description [in]

Variable of type <b>BSTR</b> that contains the new description.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

