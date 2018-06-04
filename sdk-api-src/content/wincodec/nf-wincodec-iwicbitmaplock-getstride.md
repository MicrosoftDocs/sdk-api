---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWICBitmapLock::GetStride


## -description


Provides access to the <a href="https://docs.microsoft.com/">stride</a> value for the memory.


## -parameters




### -param pcbStride [in, out]

Type: <b>UINT*</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            Note the <a href="https://docs.microsoft.com/">stride</a> value is specific to the <a href="https://msdn.microsoft.com/c0ddbc25-6abe-484b-a545-3b9376c514df">IWICBitmapLock</a>, not the bitmap. 
            For example, two consecutive locks on the same rectangle of a bitmap may return different pointers and stride values, depending on internal implementation. 
         



