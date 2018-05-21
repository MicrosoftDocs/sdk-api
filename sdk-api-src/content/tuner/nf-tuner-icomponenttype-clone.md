---
UID: NF:tuner.IComponentType.Clone
title: IComponentType::Clone
author: windows-driver-content
description: The Clone method creates a new copy of this component type.
old-location: mstv\icomponenttype_clone.htm
old-project: mstv
ms.assetid: 34cab0cb-8b38-4d03-be2a-ef14bd9505f2
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IComponentType interface, IComponentType interface [Microsoft TV Technologies],Clone method, IComponentType.Clone, IComponentType::Clone, IComponentTypeClone, mstv.icomponenttype_clone, tuner/IComponentType::Clone
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
-	IComponentType.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::Clone


## -description



The <b>Clone</b> method creates a new copy of this component type.




## -parameters




### -param NewCT






#### - ppNewCT [out]

Address of the <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface pointer that will be set to the returned interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 

