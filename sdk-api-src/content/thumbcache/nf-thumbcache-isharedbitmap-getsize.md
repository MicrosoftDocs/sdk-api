---
UID: NF:thumbcache.ISharedBitmap.GetSize
title: ISharedBitmap::GetSize
author: windows-sdk-content
description: Retrieves the size of the bitmap contained in an ISharedBitmap object.
old-location: shell\ISharedBitmap_GetSize.htm
old-project: shell
ms.assetid: 612fbb6d-2539-4055-9037-7e64ddced4e9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSize, GetSize method [Windows Shell], GetSize method [Windows Shell],ISharedBitmap interface, ISharedBitmap interface [Windows Shell],GetSize method, ISharedBitmap.GetSize, ISharedBitmap::GetSize, _shell__GetSize, shell.ISharedBitmap_GetSize, thumbcache/ISharedBitmap::GetSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - ISharedBitmap.GetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISharedBitmap::GetSize


## -description


Retrieves the size of the bitmap contained in an <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object.


## -parameters




### -param pSize [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>*</b>

When this method returns, contains a pointer to a value that specifies the size, in pixels, of the contained bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



