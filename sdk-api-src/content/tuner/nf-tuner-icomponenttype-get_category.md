---
UID: NF:tuner.IComponentType.get_Category
title: IComponentType::get_Category
author: windows-sdk-content
description: The get_Category method retrieves the component category.
old-location: mstv\icomponenttype_get_category.htm
old-project: mstv
ms.assetid: e0a61359-a15a-47f6-8388-90368867e945
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_Category method, IComponentType.get_Category, IComponentType::get_Category, IComponentTypeget_Category, get_Category, get_Category method [Microsoft TV Technologies], get_Category method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_category, tuner/IComponentType::get_Category
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentType.get_Category
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::get_Category


## -description



The <b>get_Category</b> method retrieves the component category.




## -parameters




### -param Category






#### - pCategory [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff557721">ComponentCategory</a> data type that will receive the category.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 

