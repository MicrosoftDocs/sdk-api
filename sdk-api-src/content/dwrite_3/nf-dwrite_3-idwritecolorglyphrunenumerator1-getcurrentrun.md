---
UID: NF:dwrite_3.IDWriteColorGlyphRunEnumerator1.GetCurrentRun
title: IDWriteColorGlyphRunEnumerator1::GetCurrentRun
author: windows-sdk-content
description: Gets the current color glyph run.
old-location: directwrite\idwritecolorglyphrunenumerator1_getcurrentrun.htm
tech.root: DirectWrite
ms.assetid: 0FEFD8EB-20E7-4E04-9C31-1A763D2FB816
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentRun, GetCurrentRun method [Direct Write], GetCurrentRun method [Direct Write],IDWriteColorGlyphRunEnumerator1 interface, IDWriteColorGlyphRunEnumerator1 interface [Direct Write],GetCurrentRun method, IDWriteColorGlyphRunEnumerator1.GetCurrentRun, IDWriteColorGlyphRunEnumerator1::GetCurrentRun, directwrite.idwritecolorglyphrunenumerator1_getcurrentrun, dwrite_3/IDWriteColorGlyphRunEnumerator1::GetCurrentRun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteColorGlyphRunEnumerator1.GetCurrentRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteColorGlyphRunEnumerator1::GetCurrentRun


## -description


Gets the current color glyph run.


## -parameters




### -param colorGlyphRun [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt725306(v=VS.85).aspx">DWRITE_COLOR_GLYPH_RUN1</a></b>

Receives a pointer to the color glyph run. The pointer remains valid until the next call to
          MoveNext or until the interface is released.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Standard HRESULT error code. An error is returned if there is
          no current glyph run, i.e., if MoveNext has not yet been called
          or if the end of the sequence has been reached.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt725314(v=VS.85).aspx">IDWriteColorGlyphRunEnumerator1</a>
 

 

