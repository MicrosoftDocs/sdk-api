---
UID: NS:d3d10sdklayers.D3D10_INFO_QUEUE_FILTER_DESC
title: D3D10_INFO_QUEUE_FILTER_DESC
author: windows-sdk-content
description: Allow or deny certain types of messages to pass through a filter.
old-location: direct3d10\d3d10_info_queue_filter_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_info_queue_filter_desc.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D10_INFO_QUEUE_FILTER_DESC, D3D10_INFO_QUEUE_FILTER_DESC structure [Direct3D 10], c1c85d13-4bf9-82eb-a98e-d91a114dee29, d3d10sdklayers/D3D10_INFO_QUEUE_FILTER_DESC, direct3d10.d3d10_info_queue_filter_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10sdklayers.h
req.include-header: D3D10.h
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
tech.root: 
req.typenames: D3D10_INFO_QUEUE_FILTER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10sdklayers.h
api_name:
 - D3D10_INFO_QUEUE_FILTER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_INFO_QUEUE_FILTER_DESC structure


## -description


Allow or deny certain types of messages to pass through a filter.


## -struct-fields




### -field NumCategories

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of message categories to allow or deny.


### -field pCategoryList

Type: <b><a href="https://msdn.microsoft.com/library/Bb205323(v=VS.85).aspx">D3D10_MESSAGE_CATEGORY</a>*</b>

Array of message categories to allow or deny. Array must have at least NumCategories members (see <a href="https://msdn.microsoft.com/library/Bb205323(v=VS.85).aspx">D3D10_MESSAGE_CATEGORY</a>).


### -field NumSeverities

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of message severity levels to allow or deny.


### -field pSeverityList

Type: <b><a href="https://msdn.microsoft.com/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a>*</b>

Array of message severity levels to allow or deny. Array must have at least NumSeverities members (see <a href="https://msdn.microsoft.com/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a>).


### -field NumIDs

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of message IDs to allow or deny.


### -field pIDList

Type: <b><a href="https://msdn.microsoft.com/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a>*</b>

Array of message IDs to allow or deny. Array must have at least NumIDs members (see <a href="https://msdn.microsoft.com/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a>).


## -remarks



<b>D3D10_INFO_QUEUE_FILTER_DESC</b> is used to define the allow list and deny list in the <a href="https://msdn.microsoft.com/library/Bb205313(v=VS.85).aspx">D3D10_INFO_QUEUE_FILTER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205153(v=VS.85).aspx">Core Structures</a>
 

 

