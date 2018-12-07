---
UID: NF:dwrite.IDWriteInlineObject.GetOverhangMetrics
title: IDWriteInlineObject::GetOverhangMetrics
author: windows-sdk-content
description: IDWriteTextLayout calls this callback function to get the visible extents (in DIPs) of the inline object. In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.
old-location: directwrite\idwriteinlineobject_getoverhangmetrics.htm
tech.root: DirectWrite
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOverhangMetrics, GetOverhangMetrics method [Direct Write], GetOverhangMetrics method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],GetOverhangMetrics method, IDWriteInlineObject.GetOverhangMetrics, IDWriteInlineObject::GetOverhangMetrics, directwrite.idwriteinlineobject_getoverhangmetrics, dwrite/IDWriteInlineObject::GetOverhangMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
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
 - IDWriteInlineObject.GetOverhangMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteInlineObject::GetOverhangMetrics


## -description



<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> calls this callback function to get the visible extents (in DIPs) of the inline object. In the case of a simple bitmap, with no padding and no overhang, all the overhangs will
    simply be zeroes.

The overhangs should be returned relative to the reported size of the object (see <a href="https://msdn.microsoft.com/a42d612c-3d16-4c27-a1d8-1cfb9de2f8b1">DWRITE_INLINE_OBJECT_METRICS</a>), and should not be baseline
    adjusted.


## -parameters




### -param overhangs [out]

Type: <b><a href="https://msdn.microsoft.com/a285f06b-a4d0-4ebe-80f5-157e59bfba31">DWRITE_OVERHANG_METRICS</a>*</b>

Overshoot of visible extents (in DIPs) outside the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>
 

 

