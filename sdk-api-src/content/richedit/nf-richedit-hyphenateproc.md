---
UID: NF:richedit.HyphenateProc
title: HyphenateProc function
author: windows-sdk-content
description: The HyphenateProc function is an application&#8211;defined callback function used with the EM_SETHYPHENATEINFO message. It determines how hyphenation is done in a Microsoft Rich Edit control.
old-location: controls\HyphenateProc.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditcallbackfunctions\hyphenateproc.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: HyphenateProc, HyphenateProc callback, HyphenateProc callback function [Windows Controls], _win32_HyphenateProc, _win32_HyphenateProc_cpp, controls.HyphenateProc, controls._win32_HyphenateProc, richedit/HyphenateProc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Richedit.h
api_name:
 - HyphenateProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- HyphenateProc
: 
---

# HyphenateProc function


## -description


The <i>HyphenateProc</i> function is an application–defined
		callback function used with the <a href="https://msdn.microsoft.com/en-us/library/Bb774242(v=VS.85).aspx">EM_SETHYPHENATEINFO</a> message. It determines how hyphenation is done in a Microsoft Rich Edit control.


## -parameters




### -param pszWord [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WCHAR</a>*</b>

Pointer to the word to hyphenate. 


### -param langid [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

Current language ID for the control. 


### -param ichExceed [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of the character in the passed string that exceeds the line width.


### -param phyphresult [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787932(v=VS.85).aspx">HYPHRESULT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb787932(v=VS.85).aspx">HYPHRESULT</a> structure that <i>HyphenateProc</i> fills in with the result of the hyphenation. 


## -returns



There is no return value.




## -remarks



<i>HyphenateProc</i> is a placeholder for the application-defined function name.

An application must install the callback function by specifying the address of the callback function in an <a href="https://msdn.microsoft.com/en-us/library/Bb774242(v=VS.85).aspx">EM_SETHYPHENATEINFO</a> message. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774242(v=VS.85).aspx">EM_SETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787930(v=VS.85).aspx">HYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787932(v=VS.85).aspx">HYPHRESULT</a>



<b>Reference</b>
 

 

