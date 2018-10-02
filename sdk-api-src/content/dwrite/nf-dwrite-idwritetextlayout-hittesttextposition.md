---
UID: NF:dwrite.IDWriteTextLayout.HitTestTextPosition
title: IDWriteTextLayout::HitTestTextPosition
author: windows-sdk-content
description: The application calls this function to get the pixel location relative to the top-left of the layout box given the text position and the logical side of the position.
old-location: directwrite\IDWriteTextLayout_HitTestTextPosition.htm
tech.root: DirectWrite
ms.assetid: a7a8d82a-74a6-4e4a-a57d-60194e20a087
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HitTestTextPosition, HitTestTextPosition method [Direct Write], HitTestTextPosition method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],HitTestTextPosition method, IDWriteTextLayout.HitTestTextPosition, IDWriteTextLayout::HitTestTextPosition, directwrite.IDWriteTextLayout_HitTestTextPosition, dwrite/IDWriteTextLayout::HitTestTextPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
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
 - IDWriteTextLayout.HitTestTextPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::HitTestTextPosition


## -description


 The application calls this function to get the pixel location relative
     to the top-left of the layout box given the text position and the
     logical side of the position. This function is normally used as part of
     caret positioning of text where the caret is drawn at the location
     corresponding to the current text editing position. It may also be used
     as a way to programmatically obtain the geometry of a particular text
     position in UI automation.


## -parameters




### -param textPosition

Type: <b>UINT32</b>

The text position used to get the pixel location.


### -param isTrailingHit

Type: <b>BOOL</b>

A Boolean flag that indicates whether the pixel location is of the leading or the trailing side of the specified text position.


### -param pointX [out]

Type: <b>FLOAT*</b>

When this method returns, contains the output pixel location X, relative to the top-left location of the layout box.


### -param pointY [out]

Type: <b>FLOAT*</b>

When this method returns, contains the output pixel location Y, relative to the top-left location of the layout box.


### -param hitTestMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/00aaed92-7078-4823-95c5-855c063c744a">DWRITE_HIT_TEST_METRICS</a>*</b>

When this method returns, contains the output geometry fully enclosing the specified text position.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

