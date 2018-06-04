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

# ISharedBitmap::Detach


## -description


Retrieves the bitmap contained in an <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object, and returns a copy if the contained bitmap resides in shared memory. After calling this method the bitmap is no longer associated with this <b>ISharedBitmap</b> and you cannot call <a href="https://msdn.microsoft.com/0d2cfdba-b51f-4035-b0b2-e48933505c73">ISharedBitmap::GetSharedBitmap</a> or <b>ISharedBitmap::Detach</b> on it again.


## -parameters




### -param phbm [out]

Type: <b>HBITMAP*</b>

When this method returns, contains a pointer to a handle to the bitmap to retrieve.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the bitmap being retrieved resides in shared memory, a copy of the bitmap is returned.  The <b>Detach</b> method does not release any references to the underlying shared memory.

If the bitmap being retrieved does not reside in shared memory, the bitmap itself is returned and no copy is made.



