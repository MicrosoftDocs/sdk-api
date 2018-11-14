---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetBreakOnCategory
title: ID3D10InfoQueue::SetBreakOnCategory
author: windows-sdk-content
description: Set a message category to break on when a message with that category passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_setbreakoncategory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setbreakoncategory.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 5e1bf739-ba7b-46d2-556f-7491e82f1678, ID3D10InfoQueue interface [Direct3D 10],SetBreakOnCategory method, ID3D10InfoQueue.SetBreakOnCategory, ID3D10InfoQueue::SetBreakOnCategory, SetBreakOnCategory, SetBreakOnCategory method [Direct3D 10], SetBreakOnCategory method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::SetBreakOnCategory, direct3d10.id3d10infoqueue_setbreakoncategory
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.SetBreakOnCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10sdklayers.h
: 
- ID3D10InfoQueue.SetBreakOnCategory
: 
---

# ID3D10InfoQueue::SetBreakOnCategory


## -description


Set a message category to break on when a message with that category passes through the storage filter.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/35256b90-4ba4-45ec-ad3e-a19884868740">D3D10_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="https://msdn.microsoft.com/35256b90-4ba4-45ec-ad3e-a19884868740">D3D10_MESSAGE_CATEGORY</a>).


### -param bEnable [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

