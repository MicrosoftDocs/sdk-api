---
UID: NF:t2embapi.TTIsEmbeddingEnabled
title: TTIsEmbeddingEnabled function
author: windows-sdk-content
description: Determines whether the typeface exclusion list contains a specified font.
old-location: gdi\ttisembeddingenabled.htm
tech.root: gdi
ms.assetid: f1e3112b-d840-45eb-bb99-416319ed9e15
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TTIsEmbeddingEnabled, TTIsEmbeddingEnabled function [Windows GDI], _win32_TTIsEmbeddingEnabled, gdi.ttisembeddingenabled, t2embapi/TTIsEmbeddingEnabled
ms.topic: function
req.header: t2embapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - T2embed.dll
api_name:
 - TTIsEmbeddingEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TTIsEmbeddingEnabled function


## -description


Determines whether the typeface exclusion list contains a specified font.


## -parameters




### -param hDC [in]

Device context handle.


### -param pbEnabled [out]

Pointer to a boolean, set upon completion of the function. A nonzero value indicates the font is not in the typeface exclusion list and, therefore, can be embedded without conflict.


## -returns



If successful, returns E_NONE.

The parameter <i>pbEnabled</i> is filled with a boolean that indicates whether embedding is currently enabled within a device context.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



If the specified font is listed, the client should not embed the font.

For additional information on the exclusion list, see the Remarks section of <a href="https://msdn.microsoft.com/05d74bfb-28c4-4e1a-9e18-df868f8fa784">TTEnableEmbeddingForFacename</a>.




## -see-also




<a href="https://msdn.microsoft.com/05d74bfb-28c4-4e1a-9e18-df868f8fa784">TTEnableEmbeddingForFacename</a>



<a href="https://msdn.microsoft.com/0ce9ade0-df5b-4a2a-adf6-ca641e27d2bd">TTGetEmbeddedFontInfo</a>



<a href="https://msdn.microsoft.com/c442447f-221d-4bce-9749-fb9fbe333808">TTGetEmbeddingType</a>



<a href="https://msdn.microsoft.com/1f494bb1-62c4-45c4-b1a5-df6842d94dcc">TTIsEmbeddingEnabledForFacename</a>
 

 

