---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnCategory
title: ID3D10InfoQueue::GetBreakOnCategory
author: windows-driver-content
description: Get a message category to break on when a message with that category passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_getbreakoncategory.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakoncategory.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetBreakOnCategory, GetBreakOnCategory method [Direct3D 10], GetBreakOnCategory method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnCategory method, ID3D10InfoQueue.GetBreakOnCategory, ID3D10InfoQueue::GetBreakOnCategory, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnCategory, direct3d10.id3d10infoqueue_getbreakoncategory, f7712289-f56a-df8e-a2dd-2568f07262a8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10sdklayers.h
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10SDKLayers.h
api_name:
-	ID3D10InfoQueue.GetBreakOnCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::GetBreakOnCategory


## -description


Get a message category to break on when a message with that category passes through the storage filter.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/35256b90-4ba4-45ec-ad3e-a19884868740">D3D10_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="https://msdn.microsoft.com/35256b90-4ba4-45ec-ad3e-a19884868740">D3D10_MESSAGE_CATEGORY</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

