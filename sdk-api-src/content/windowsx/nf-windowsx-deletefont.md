---
UID: NF:windowsx.DeleteFont
title: DeleteFont macro
author: windows-sdk-content
description: The DeleteFont macro deletes a font object, freeing all system resources associated with the font object.
old-location: gdi\deletefont.htm
tech.root: gdi
ms.assetid: 5cb6c667-3c8b-41cf-b2b7-9e1e89729da7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DeleteFont, DeleteFont macro [Windows GDI], _win32_DeleteFont, gdi.deletefont, windowsx/DeleteFont
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DeleteFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteFont macro


## -description



The <b>DeleteFont</b> macro deletes a font object, freeing all system resources associated with the font object.




## -parameters




### -param hfont

A handle to the font object.


## -remarks



After the font object is deleted, the specified handle is no longer valid.

The <b>DeleteFont</b> macro is equivalent to calling <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> as follows:

<pre class="syntax" xml:space="preserve"><code>
   DeleteObject((HGDIOBJ)(HFONT)(hfont))
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/e7c145aa-566d-4754-a4dd-a5e71e188258">SelectFont</a>
 

 

