---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetBreakOnCategory
title: ID3D11InfoQueue::GetBreakOnCategory
author: windows-sdk-content
description: Get a message category to break on when a message with that category passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_getbreakoncategory.htm
old-project: direct3d11
ms.assetid: 747755ec-3260-4ded-9c36-efdf1a90adcb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 08043309-7517-83fc-be14-01f7cb816e88, GetBreakOnCategory, GetBreakOnCategory method [Direct3D 11], GetBreakOnCategory method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetBreakOnCategory method, ID3D11InfoQueue.GetBreakOnCategory, ID3D11InfoQueue::GetBreakOnCategory, d3d11sdklayers/ID3D11InfoQueue::GetBreakOnCategory, direct3d11.id3d11infoqueue_getbreakoncategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.GetBreakOnCategory
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::GetBreakOnCategory


## -description


Get a message category to break on when a message with that category passes through the storage filter.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

