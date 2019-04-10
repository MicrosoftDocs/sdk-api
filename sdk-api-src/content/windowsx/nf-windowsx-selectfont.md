---
UID: NF:windowsx.SelectFont
title: SelectFont macro (windowsx.h)
author: windows-sdk-content
description: The SelectFont macro selects a font object into the specified device context (DC). The new font object replaces the previous font object.
old-location: gdi\selectfont.htm
tech.root: gdi
ms.assetid: e7c145aa-566d-4754-a4dd-a5e71e188258
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SelectFont, SelectFont macro [Windows GDI], _win32_SelectFont, gdi.selectfont, windowsx/SelectFont
ms.topic: macro
req.header: windowsx.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - SelectFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SelectFont macro


## -description



The <b>SelectFont</b> macro selects a font object into the specified device context (DC). The new font object replaces the previous font object.




## -parameters




### -param hdc

A handle to the DC.


### -param hfont

A handle to the font object to be selected. The font object must have been created using either <a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a> or <a href="https://msdn.microsoft.com/b7919fb6-8515-4f1b-af9c-dc7eac381b90">CreateFontIndirect</a>.


## -remarks



After an application has finished drawing with the new font object, it should always replace a new font object with the original font object.

The <b>SelectFont</b> macro is equivalent to calling <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> as follows:

<pre class="syntax" xml:space="preserve"><code>
((HFONT) SelectObject((hdc), (HGDIOBJ)(HFONT)(hfont)))
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/5cb6c667-3c8b-41cf-b2b7-9e1e89729da7">DeleteFont</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

