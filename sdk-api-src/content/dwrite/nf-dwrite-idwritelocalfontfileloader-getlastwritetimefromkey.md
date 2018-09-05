---
UID: NF:dwrite.IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
title: IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey
author: windows-sdk-content
description: Obtains the last write time of the file from the font file reference key.
old-location: directwrite\idwritelocalfontfileloader_getlastwritetimefromkey.htm
old-project: DirectWrite
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetLastWriteTimeFromKey, GetLastWriteTimeFromKey method [Direct Write], GetLastWriteTimeFromKey method [Direct Write],IDWriteLocalFontFileLoader interface, IDWriteLocalFontFileLoader interface [Direct Write],GetLastWriteTimeFromKey method, IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey, IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey, directwrite.idwritelocalfontfileloader_getlastwritetimefromkey, dwrite/IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
 - IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey


## -description


Obtains the last write time of the file from the font file reference key.


## -parameters




### -param fontFileReferenceKey [in]

Type: <b>const void*</b>

The font file reference key that uniquely identifies the local font file
    within the scope of the font loader being used.


### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

The size of font file reference key in bytes.


### -param lastWriteTime [out]

Type: <b>FILETIME*</b>

The time of the last font file modification.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/acb777c8-24c6-452e-8f58-8fb2ad8c0b6c">IDWriteLocalFontFileLoader</a>
 

 

