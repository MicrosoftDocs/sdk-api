---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetBreakOnCategory
title: ID3D11InfoQueue::SetBreakOnCategory
author: windows-sdk-content
description: Set a message category to break on when a message with that category passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_setbreakoncategory.htm
old-project: direct3d11
ms.assetid: 3d6f66bf-01b8-4bab-a40e-98f5893050cd
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 17afaa7e-0f5c-964c-84e9-887599f0d947, ID3D11InfoQueue interface [Direct3D 11],SetBreakOnCategory method, ID3D11InfoQueue.SetBreakOnCategory, ID3D11InfoQueue::SetBreakOnCategory, SetBreakOnCategory, SetBreakOnCategory method [Direct3D 11], SetBreakOnCategory method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetBreakOnCategory, direct3d11.id3d11infoqueue_setbreakoncategory
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11InfoQueue.SetBreakOnCategory
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::SetBreakOnCategory


## -description


Set a message category to break on when a message with that category passes through the storage filter.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a>).


### -param bEnable [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

