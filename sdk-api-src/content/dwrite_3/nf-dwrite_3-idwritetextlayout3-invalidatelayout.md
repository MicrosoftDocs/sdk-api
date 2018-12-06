---
UID: NF:dwrite_3.IDWriteTextLayout3.InvalidateLayout
title: IDWriteTextLayout3::InvalidateLayout
author: windows-sdk-content
description: Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions. This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.
old-location: directwrite\idwritetextlayout3_invalidatelayout.htm
tech.root: DirectWrite
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextLayout3 interface [Direct Write],InvalidateLayout method, IDWriteTextLayout3.InvalidateLayout, IDWriteTextLayout3::InvalidateLayout, InvalidateLayout, InvalidateLayout method [Direct Write], InvalidateLayout method [Direct Write],IDWriteTextLayout3 interface, directwrite.idwritetextlayout3_invalidatelayout, dwrite_3/IDWriteTextLayout3::InvalidateLayout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDWriteTextLayout3.InvalidateLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout3::InvalidateLayout


## -description


Invalidates the layout, forcing layout to remeasure before calling the   
   metrics or drawing functions. This is useful if the locality of a font    
   changes, and layout should be redrawn, or if the size of a client    
   implemented IDWriteInlineObject changes. 


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a7741740-9524-caf0-650b-56808abcf328">IDWriteTextLayout3</a>
 

 

