---
UID: NS:strmif._FilterInfo
title: "_FilterInfo"
author: windows-sdk-content
description: The FILTER_INFO structure contains information about a filter.
old-location: dshow\filter_info.htm
tech.root: DirectShow
ms.assetid: 43d1951e-448d-4139-879b-3fe021490d7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FILTER_INFO, FILTER_INFO structure [DirectShow], FILTER_INFOStructure, _FilterInfo, dshow.filter_info, strmif/FILTER_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
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
 - strmif.h
api_name:
 - FILTER_INFO
product: Windows
targetos: Windows
req.typenames: FILTER_INFO
req.redist: 
---

# _FilterInfo structure


## -description



The <code>FILTER_INFO</code> structure contains information about a filter.




## -struct-fields




### -field achName

Null-terminated string containing the name of the filter.


### -field pGraph

If the filter is member of a filter graph, contains a pointer to the filter graph's <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> interface. If the filter is not a member of a filter graph, this value of this member is <b>NULL</b>.


## -remarks



If the <b>pGraph</b> member is not <b>NULL</b>, the application should release the <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> interface when it is finished using it.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

