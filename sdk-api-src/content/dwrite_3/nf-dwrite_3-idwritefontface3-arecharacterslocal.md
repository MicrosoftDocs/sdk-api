---
UID: NF:dwrite_3.IDWriteFontFace3.AreCharactersLocal
title: IDWriteFontFace3::AreCharactersLocal
author: windows-sdk-content
description: Determines whether the specified characters are local.
old-location: directwrite\idwritefontface3_arecharacterslocal.htm
tech.root: DirectWrite
ms.assetid: 4cbb6895-3151-c6dd-881e-50d3532c8a14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AreCharactersLocal, AreCharactersLocal method [Direct Write], AreCharactersLocal method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],AreCharactersLocal method, IDWriteFontFace3.AreCharactersLocal, IDWriteFontFace3::AreCharactersLocal, directwrite.idwritefontface3_arecharacterslocal, dwrite_3/IDWriteFontFace3::AreCharactersLocal
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
 - IDWriteFontFace3.AreCharactersLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace3::AreCharactersLocal


## -description


Determines whether the specified characters are local.


## -parameters




### -param characters [in]

Type: <b>WCHAR</b>

Array of characters.


### -param characterCount

Type: <b>UINT32</b>

The number of elements in the character array.


### -param enqueueIfNotLocal

Type: <b>BOOL</b>

Specifies whether to enqueue a download request    
       if any of the specified characters are not local.


### -param isLocal [out]

Type: <b>BOOL*</b>

Receives TRUE if all of the specified characters are local,    
       FALSE if any of the specified characters are remote.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894561(v=VS.85).aspx">IDWriteFontFace3</a>
 

 

