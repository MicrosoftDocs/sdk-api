---
UID: NE:d2d1.D2D1_TEXT_ANTIALIAS_MODE
title: D2D1_TEXT_ANTIALIAS_MODE
author: windows-sdk-content
description: Describes the antialiasing mode used for drawing text.
old-location: direct2d\D2D1_TEXT_ANTIALIAS_MODE.htm
tech.root: direct2d
ms.assetid: d2c829d7-9892-4cbb-9993-12bb7d77fc25
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D2D1_TEXT_ANTIALIAS_MODE, D2D1_TEXT_ANTIALIAS_MODE enumeration [Direct2D], D2D1_TEXT_ANTIALIAS_MODE_ALIASED, D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE, D2D1_TEXT_ANTIALIAS_MODE_DEFAULT, D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE, d2d1/D2D1_TEXT_ANTIALIAS_MODE, d2d1/D2D1_TEXT_ANTIALIAS_MODE_ALIASED, d2d1/D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE, d2d1/D2D1_TEXT_ANTIALIAS_MODE_DEFAULT, d2d1/D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE, direct2d.D2D1_TEXT_ANTIALIAS_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_TEXT_ANTIALIAS_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_TEXT_ANTIALIAS_MODE
req.redist: 
---

# D2D1_TEXT_ANTIALIAS_MODE enumeration


## -description


Describes the antialiasing mode used for drawing text.


## -enum-fields




### -field D2D1_TEXT_ANTIALIAS_MODE_DEFAULT

Use the system default. See Remarks.


### -field D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE

Use ClearType antialiasing.


### -field D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE

Use grayscale antialiasing.


### -field D2D1_TEXT_ANTIALIAS_MODE_ALIASED

Do not use antialiasing.


### -field D2D1_TEXT_ANTIALIAS_MODE_FORCE_DWORD




## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a> of an <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> to specify how text and glyphs are antialiased.

 By default, Direct2D renders text in ClearType mode. Factors that 

can downgrade the default quality to grayscale or aliased:

<ul>
<li>If the <a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a> value  is <b>DWRITE_RENDERING_MODE_ALIASED </b>, then the 

default text antialiasing mode is aliased.  To change the DirectWrite rendering mode of an <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>, use the  <a href="https://msdn.microsoft.com/ab4b29a5-72a7-49dc-9131-696f888b0355">ID2D1RenderTarget::SetTextRenderingParams</a> method. </li>
<li>If the <a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a> value is <b>DWRITE_RENDERING_MODE_OUTLINE</b>, then the default text 

antialiasing mode is grayscale.</li>
<li>If the render target has an alpha channel and is not set to <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_IGNORE</a>, then 

the default text antialiasing mode is grayscale.</li>
<li>If <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">ID2D1RenderTarget::PushLayer</a>  is called without <a href="https://msdn.microsoft.com/d278211a-e99c-429d-9752-45c305f52ed8">D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE</a> 

(and the corresponding <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> has not  been called yet), then the default text 

antialiasing mode is grayscale.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">ID2D1RenderTarget::SetTextAntialiasMode</a>



<a href="https://msdn.microsoft.com/ab4b29a5-72a7-49dc-9131-696f888b0355">ID2D1RenderTarget::SetTextRenderingParams</a>
 

 

