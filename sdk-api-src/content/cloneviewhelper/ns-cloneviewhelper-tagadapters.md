---
UID: NS:cloneviewhelper.tagAdapters
title: tagAdapters
author: windows-sdk-content
description: The Adapters structure contains a list of graphics adapters.
old-location: display\adapters.htm
tech.root: Display
ms.assetid: 4f91e683-66f6-4667-86d0-d3de28ba64b0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Adapters, Adapters structure [Display Devices], TMM_Ref_5b0d959d-9d91-4166-8555-633b0690de8a.xml, cloneviewhelper/Adapters, display.adapters, tagAdapters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - cloneviewhelper.h
api_name:
 - Adapters
product: Windows
targetos: Windows
req.typenames: Adapters
req.redist: 
---

# tagAdapters structure


## -description


The Adapters structure contains a list of graphics adapters. 


## -struct-fields




### -field numAdapters

The number of graphics adapters in the array that the <b>adapter</b> member specifies. 


### -field adapter

An array of <a href="https://msdn.microsoft.com/c62c6aed-2593-4b5d-884f-99d20e269eb1">Adapter</a> structures that specify information about graphics adapters. 


## -see-also




<a href="https://msdn.microsoft.com/c62c6aed-2593-4b5d-884f-99d20e269eb1">Adapter</a>



<a href="https://msdn.microsoft.com/8ec09950-afb6-43ff-8e05-4c801e49ba4b">IViewHelper::SetConfiguration</a>
 

 

