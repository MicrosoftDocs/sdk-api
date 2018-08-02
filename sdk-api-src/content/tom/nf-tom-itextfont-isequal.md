---
UID: NF:tom.ITextFont.IsEqual
title: ITextFont::IsEqual
author: windows-sdk-content
description: Determines whether this text font object has the same properties as the specified text font object.
old-location: controls\ITextFont_IsEqual.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontisequal.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextFont interface [Windows Controls],IsEqual method, ITextFont.IsEqual, ITextFont::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextFont interface, _win32_ITextFont_IsEqual, _win32_ITextFont_IsEqual_cpp, controls.ITextFont_IsEqual, controls._win32_ITextFont_IsEqual, tom/ITextFont::IsEqual
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
 - ITextFont.IsEqual
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::IsEqual


## -description


Determines whether this text font object has the same properties as the specified text font object.


## -parameters




### -param pFont

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>*</b>

The text font object to compare against.


### -param pValue






#### - pB

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the font objects have the same properties or <b>tomFalse</b> if they do not. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If the text font objects have the same properties, the method succeeds and returns <b>S_OK</b>. If the text font objects do not have the same properties, the method fails and returns <b>S_FALSE</b>. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



The text font objects are equal only if <i>pFont</i> belongs to the same Text Object Model (TOM) object as the current font object. The <b>ITextFont::IsEqual</b> method ignores entries for which either font object has an <a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomUndefined</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

