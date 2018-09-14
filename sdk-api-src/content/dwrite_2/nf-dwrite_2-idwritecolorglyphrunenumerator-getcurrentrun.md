---
UID: NF:dwrite_2.IDWriteColorGlyphRunEnumerator.GetCurrentRun
title: IDWriteColorGlyphRunEnumerator::GetCurrentRun
author: windows-sdk-content
description: Returns the current glyph run of the enumerator.
old-location: directwrite\idwritecolorglyphrunenumerator_getcurrentrun.htm
tech.root: DirectWrite
ms.assetid: F4D89E35-3846-41F0-A724-3648DC9D487E
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetCurrentRun, GetCurrentRun method [Direct Write], GetCurrentRun method [Direct Write],IDWriteColorGlyphRunEnumerator interface, IDWriteColorGlyphRunEnumerator interface [Direct Write],GetCurrentRun method, IDWriteColorGlyphRunEnumerator.GetCurrentRun, IDWriteColorGlyphRunEnumerator::GetCurrentRun, directwrite.idwritecolorglyphrunenumerator_getcurrentrun, dwrite_2/IDWriteColorGlyphRunEnumerator::GetCurrentRun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDWriteColorGlyphRunEnumerator.GetCurrentRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteColorGlyphRunEnumerator::GetCurrentRun


## -description


Returns the current glyph run of the enumerator.


## -parameters




### -param colorGlyphRun [out]

Type: <b>const <a href="https://msdn.microsoft.com/E70CEE54-80BB-42D2-BBD7-97472AAA4B56">DWRITE_COLOR_GLYPH_RUN</a>**</b>

A pointer to the current glyph run.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/649AD648-32BB-4BF4-A82F-075E93505E33">IDWriteColorGlyphRunEnumerator</a>
 

 

