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
 

 

