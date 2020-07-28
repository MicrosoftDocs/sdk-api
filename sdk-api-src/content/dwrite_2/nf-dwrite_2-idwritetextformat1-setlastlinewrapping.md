---
UID: NF:dwrite_2.IDWriteTextFormat1.SetLastLineWrapping
title: IDWriteTextFormat1::SetLastLineWrapping (dwrite_2.h)
description: Sets the wrapping mode of the last line.
helpviewer_keywords: ["IDWriteTextFormat1 interface [Direct Write]","SetLastLineWrapping method","IDWriteTextFormat1.SetLastLineWrapping","IDWriteTextFormat1::SetLastLineWrapping","SetLastLineWrapping","SetLastLineWrapping method [Direct Write]","SetLastLineWrapping method [Direct Write]","IDWriteTextFormat1 interface","directwrite.idwritetextformat1_setwraponlastline","dwrite_2/IDWriteTextFormat1::SetLastLineWrapping"]
old-location: directwrite\idwritetextformat1_setwraponlastline.htm
tech.root: DirectWrite
ms.assetid: 2A842924-B925-4F16-A1A0-997142233AA9
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat1 interface [Direct Write],SetLastLineWrapping method, IDWriteTextFormat1.SetLastLineWrapping, IDWriteTextFormat1::SetLastLineWrapping, SetLastLineWrapping, SetLastLineWrapping method [Direct Write], SetLastLineWrapping method [Direct Write],IDWriteTextFormat1 interface, directwrite.idwritetextformat1_setwraponlastline, dwrite_2/IDWriteTextFormat1::SetLastLineWrapping
f1_keywords:
- dwrite_2/IDWriteTextFormat1.SetLastLineWrapping
dev_langs:
- c++
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteTextFormat1.SetLastLineWrapping
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextFormat1::SetLastLineWrapping


## -description


Sets the wrapping mode of the last line.


## -parameters




### -param isLastLineWrappingEnabled

Type: <b>BOOL</b>

If set to FALSE, the last line is not wrapped. If set to TRUE, the last line is wrapped.

The last line is wrapped by default.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/DirectWrite/idwritetextformat1">IDWriteTextFormat1</a>
 

 

