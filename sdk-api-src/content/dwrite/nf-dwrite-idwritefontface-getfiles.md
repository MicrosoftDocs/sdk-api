---
UID: NF:dwrite.IDWriteFontFace.GetFiles
title: IDWriteFontFace::GetFiles
author: windows-sdk-content
description: Obtains the font files representing a font face.
old-location: directwrite\IDWriteFontFace_GetFiles.htm
old-project: DirectWrite
ms.assetid: 505238e5-bfc9-4d5e-b807-3c5e8b2e82d3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetFiles, GetFiles method [Direct Write], GetFiles method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetFiles method, IDWriteFontFace.GetFiles, IDWriteFontFace::GetFiles, directwrite.IDWriteFontFace_GetFiles, dwrite/IDWriteFontFace::GetFiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace.GetFiles
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFace::GetFiles


## -description


 Obtains the font files representing a font face.


## -parameters




### -param numberOfFiles [in, out]

Type: <b>UINT32*</b>

If <i>fontFiles</i> is <b>NULL</b>, receives the number of files representing the font face.  Otherwise, the number of font files being requested should be passed.  See the Remarks section below for more information.


### -param fontFiles [out, optional]

Type: <b><a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a>**</b>

When this method returns, contains a pointer to a user-provided array that stores pointers to font files representing the font face.
     This parameter can be <b>NULL</b> if the user wants only the number of files representing the font face.
     This API increments reference count of the font file pointers returned according to COM conventions, and the client
     should release them when finished.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IDWriteFontFace::GetFiles</b> method should be called twice.  The first time you call <b>GetFiles</b><i>fontFiles</i> should be <b>NULL</b>. When the method returns, <i>numberOfFiles</i> receives the number of font files that represent the font face.

Then, call the method a second time, passing the <i>numberOfFiles</i> value that was output the first call, and a non-null buffer of the correct size to store the <a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a> pointers.




## -see-also




<a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>
 

 

