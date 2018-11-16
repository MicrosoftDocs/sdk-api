---
UID: NS:d3d11sdklayers.D3D11_INFO_QUEUE_FILTER_DESC
title: D3D11_INFO_QUEUE_FILTER_DESC
author: windows-sdk-content
description: Allow or deny certain types of messages to pass through a filter.
old-location: direct3d11\d3d11_info_queue_filter_desc.htm
tech.root: direct3d11
ms.assetid: 265aa51a-7352-4d3a-b523-9e497e1e6a94
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 06785e69-a7e6-f154-5f99-7c38c12d6958, D3D11_INFO_QUEUE_FILTER_DESC, D3D11_INFO_QUEUE_FILTER_DESC structure [Direct3D 11], d3d11sdklayers/D3D11_INFO_QUEUE_FILTER_DESC, direct3d11.d3d11_info_queue_filter_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of message categories to allow or deny.


### -field pCategoryList

Type: <b><a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a>*</b>

Array of message categories to allow or deny. Array must have at least NumCategories members (see <a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a>).


### -field NumSeverities

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of message severity levels to allow or deny.


### -field pSeverityList

Type: <b><a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a>*</b>

Array of message severity levels to allow or deny. Array must have at least NumSeverities members (see <a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a>).


### -field NumIDs

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of message IDs to allow or deny.


### -field pIDList

Type: <b><a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a>*</b>

Array of message IDs to allow or deny. Array must have at least NumIDs members (see <a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a>).


## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/65f0830f-f009-47fb-b04e-24790e677338">Layer Structures</a>
 

 

