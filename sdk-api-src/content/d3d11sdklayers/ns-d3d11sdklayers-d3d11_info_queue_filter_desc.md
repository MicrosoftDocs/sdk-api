---
UID: NS:d3d11sdklayers.D3D11_INFO_QUEUE_FILTER_DESC
title: D3D11_INFO_QUEUE_FILTER_DESC
author: windows-sdk-content
description: Allow or deny certain types of messages to pass through a filter.
old-location: direct3d11\d3d11_info_queue_filter_desc.htm
tech.root: direct3d11
ms.assetid: 265aa51a-7352-4d3a-b523-9e497e1e6a94
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 06785e69-a7e6-f154-5f99-7c38c12d6958, D3D11_INFO_QUEUE_FILTER_DESC, D3D11_INFO_QUEUE_FILTER_DESC structure [Direct3D 11], d3d11sdklayers/D3D11_INFO_QUEUE_FILTER_DESC, direct3d11.d3d11_info_queue_filter_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11sdklayers.h
req.include-header: 
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
 - D3D11SDKLayers.h
api_name:
 - D3D11_INFO_QUEUE_FILTER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_INFO_QUEUE_FILTER_DESC
req.redist: 
---

# D3D11_INFO_QUEUE_FILTER_DESC structure


## -description


Allow or deny certain types of messages to pass through a filter.


## -struct-fields




### -field NumCategories

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of message categories to allow or deny.


### -field pCategoryList

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476185(v=VS.85).aspx">D3D11_MESSAGE_CATEGORY</a>*</b>

Array of message categories to allow or deny. Array must have at least NumCategories members (see <a href="https://msdn.microsoft.com/en-us/library/Ff476185(v=VS.85).aspx">D3D11_MESSAGE_CATEGORY</a>).


### -field NumSeverities

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of message severity levels to allow or deny.


### -field pSeverityList

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a>*</b>

Array of message severity levels to allow or deny. Array must have at least NumSeverities members (see <a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a>).


### -field NumIDs

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of message IDs to allow or deny.


### -field pIDList

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a>*</b>

Array of message IDs to allow or deny. Array must have at least NumIDs members (see <a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a>).


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476159(v=VS.85).aspx">Layer Structures</a>
 

 

