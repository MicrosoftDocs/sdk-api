---
UID: NS:cloneviewhelper.tagAdapter
title: tagAdapter
author: windows-sdk-content
description: The Adapter structure describes a graphics adapter.
old-location: display\adapter.htm
tech.root: display
ms.assetid: c62c6aed-2593-4b5d-884f-99d20e269eb1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Adapter, Adapter structure [Display Devices], TMM_Ref_6570c45d-9024-46c4-bcd4-848eb2d18955.xml, cloneviewhelper/Adapter, display.adapter, tagAdapter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Adapter
product: Windows
targetos: Windows
req.typenames: Adapter
req.redist: 
---

# tagAdapter structure


## -description


The Adapter structure describes a graphics adapter. 


## -struct-fields




### -field AdapterName

A single wide-character string that holds the name of the graphics adapter. 


### -field numSources

The number of video present sources in the array that the <b>sources</b> member specifies. 


### -field sources

An array of <a href="https://msdn.microsoft.com/5fbb12bc-d6e0-4cb7-b9d7-4e28ad85eca2">Sources</a> structures that specify a list of Video Present Network (VidPN) topologies. 


## -see-also




<a href="https://msdn.microsoft.com/8ec09950-afb6-43ff-8e05-4c801e49ba4b">IViewHelper::SetConfiguration</a>



<a href="https://msdn.microsoft.com/5fbb12bc-d6e0-4cb7-b9d7-4e28ad85eca2">Sources</a>
 

 

