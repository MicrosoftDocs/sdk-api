---
UID: NF:dwrite.IDWriteTextLayout.SetInlineObject
title: IDWriteTextLayout::SetInlineObject (dwrite.h)
author: windows-sdk-content
description: Sets the inline object.
old-location: directwrite\IDWriteTextLayout_SetInlineObject.htm
tech.root: DirectWrite
ms.assetid: 19fc9dd8-d732-4078-9db3-bad18681c7ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetInlineObject method, IDWriteTextLayout.SetInlineObject, IDWriteTextLayout::SetInlineObject, SetInlineObject, SetInlineObject method [Direct Write], SetInlineObject method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetInlineObject, dwrite/IDWriteTextLayout::SetInlineObject
ms.topic: method
f1_keywords: 
 - "dwrite/IDWriteTextLayout.SetInlineObject"
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
 - IDWriteTextLayout.SetInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout::SetInlineObject


## -description


 Sets the inline object.


## -parameters




### -param inlineObject

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>*</b>

An application-defined inline object. 


### -param textRange

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The application may call this function to specify the set of properties describing an application-defined inline object for specific range.

 This inline object applies to the specified range and will be passed back
     to the application by way of the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject">DrawInlineObject</a> callback when the range is drawn.
     Any text in that range will be suppressed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>
 

 

