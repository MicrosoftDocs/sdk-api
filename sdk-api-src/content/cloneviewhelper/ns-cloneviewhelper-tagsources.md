---
UID: NS:cloneviewhelper.tagSources
title: tagSources
author: windows-sdk-content
description: The Sources structure contains a Video Present Network (VidPN) topology.
old-location: display\sources.htm
old-project: display
ms.assetid: 5fbb12bc-d6e0-4cb7-b9d7-4e28ad85eca2
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: Sources, Sources structure [Display Devices], TMM_Ref_e15dfa1e-b8f8-464e-b683-c968113fbf64.xml, cloneviewhelper/Sources, display.sources, tagSources
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.redist: 
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cloneviewhelper.h
api_name:
 - Sources
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagSources structure


## -description


The Sources structure contains a Video Present Network (VidPN) topology. 


## -struct-fields




### -field sourceId

The source identifier for the video present source in the VidPN topology. 


### -field numTargets

The number of video present targets in the array that the <b>aTargets</b> member specifies, which is the number of video present targets in the VidPN topology. 


### -field aTargets

An array of identifiers for the video present targets in the VidPN topology. 


## -see-also




<a href="https://msdn.microsoft.com/c62c6aed-2593-4b5d-884f-99d20e269eb1">Adapter</a>



<a href="https://msdn.microsoft.com/8ec09950-afb6-43ff-8e05-4c801e49ba4b">IViewHelper::SetConfiguration</a>
 

 

