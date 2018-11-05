---
UID: NF:tom.ITextFont.CanChange
title: ITextFont::CanChange
author: windows-sdk-content
description: Determines whether the font can be changed.
old-location: controls\ITextFont_CanChange.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontcanchange.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CanChange, CanChange method [Windows Controls], CanChange method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],CanChange method, ITextFont.CanChange, ITextFont::CanChange, _win32_ITextFont_CanChange, _win32_ITextFont_CanChange_cpp, controls.ITextFont_CanChange, controls._win32_ITextFont_CanChange, tom/ITextFont::CanChange
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
 - ITextFont.CanChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::CanChange


## -description


Determines whether the font can be changed. 


## -parameters




### -param pValue

TBD




#### - pbCanChange [retval]

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the font can be changed or <b>tomFalse</b> if it cannot be changed. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If the font can change, the method returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font cannot change.

</td>
</tr>
</table>
 




## -remarks



The *<i>pbCanChange</i> returns <b>tomTrue</b> only if the font can be changed. That is, no part of an associated range is protected and an associated document is not read-only. If this <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> object is a duplicate, no protection rules apply.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

