---
UID: NF:tom.ITextRange.GetFont
title: ITextRange::GetFont
author: windows-sdk-content
description: Gets an ITextFont object with the character attributes of the specified range.
old-location: controls\ITextRange_GetFont.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getfont.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFont, GetFont method [Windows Controls], GetFont method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetFont method, ITextRange.GetFont, ITextRange::GetFont, _win32_ITextRange_GetFont, _win32_ITextRange_GetFont_cpp, controls.ITextRange_GetFont, controls._win32_ITextRange_GetFont, tom/ITextRange::GetFont
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetFont


## -description


Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> object with the character attributes of the specified range.


## -parameters




### -param ppFont

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>**</b>

The pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> object. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>ppFont</i> is null, the method fails and it returns E_INVALIDARG.




## -remarks



For plain-text controls, these objects do not vary from range to range, but in rich-text solutions, they do. See the section on <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> for further details.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

