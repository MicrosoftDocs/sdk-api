---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

