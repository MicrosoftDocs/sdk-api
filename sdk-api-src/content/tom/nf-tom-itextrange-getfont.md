---
UID: NF:tom.ITextRange.GetFont
title: ITextRange::GetFont
author: windows-sdk-content
description: Gets an ITextFont object with the character attributes of the specified range.
old-location: controls\ITextRange_GetFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getfont.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetFont, GetFont method [Windows Controls], GetFont method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetFont method, ITextRange.GetFont, ITextRange::GetFont, _win32_ITextRange_GetFont, _win32_ITextRange_GetFont_cpp, controls.ITextRange_GetFont, controls._win32_ITextRange_GetFont, tom/ITextRange::GetFont
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.GetFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::GetFont


## -description


Gets an <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> object with the character attributes of the specified range.


## -parameters




### -param ppFont

Type: <b><a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>**</b>

The pointer to an <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> object. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>ppFont</i> is null, the method fails and it returns E_INVALIDARG.




## -remarks



For plain-text controls, these objects do not vary from range to range, but in rich-text solutions, they do. See the section on <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> for further details.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

