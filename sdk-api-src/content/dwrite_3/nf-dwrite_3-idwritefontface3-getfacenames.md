---
UID: NF:dwrite_3.IDWriteFontFace3.GetFaceNames
title: IDWriteFontFace3::GetFaceNames (dwrite_3.h)
author: windows-sdk-content
description: Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.
old-location: directwrite\idwritefontface3_getfacenames.htm
tech.root: DirectWrite
ms.assetid: 81FBE594-3429-4E61-9A83-513605879D2D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFaceNames, GetFaceNames method [Direct Write], GetFaceNames method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetFaceNames method, IDWriteFontFace3.GetFaceNames, IDWriteFontFace3::GetFaceNames, directwrite.idwritefontface3_getfacenames, dwrite_3/IDWriteFontFace3::GetFaceNames
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFace3.GetFaceNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace3::GetFaceNames


## -description


Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.


## -parameters




### -param names [out]

Type: <b><a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a> interface for the newly created localized strings object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1081A005-E4A8-4EE0-AFE0-10BD8D8471DF">IDWriteFontFace3</a>
 

 

