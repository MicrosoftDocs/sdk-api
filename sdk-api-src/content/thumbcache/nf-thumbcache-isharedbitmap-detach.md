---
UID: NF:thumbcache.ISharedBitmap.Detach
title: ISharedBitmap::Detach
author: windows-sdk-content
description: Retrieves the bitmap contained in an ISharedBitmap object, and returns a copy if the contained bitmap resides in shared memory.
old-location: shell\ISharedBitmap_Detach.htm
tech.root: shell
ms.assetid: 1d68beca-c254-435e-a1cd-04e7aa462c84
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: Detach, Detach method [Windows Shell], Detach method [Windows Shell],ISharedBitmap interface, ISharedBitmap interface [Windows Shell],Detach method, ISharedBitmap.Detach, ISharedBitmap::Detach, _shell__Detach, shell.ISharedBitmap_Detach, thumbcache/ISharedBitmap::Detach
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
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
 - Thumbcache.h
api_name:
 - ISharedBitmap.Detach
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



