---
UID: NF:tom.ITextFont.GetLanguageID
title: ITextFont::GetLanguageID
author: windows-sdk-content
description: Gets the language ID or language code identifier (LCID).
old-location: controls\ITextFont_GetLanguageID.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlanguageid.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLanguageID, GetLanguageID method [Windows Controls], GetLanguageID method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetLanguageID method, ITextFont.GetLanguageID, ITextFont::GetLanguageID, _win32_ITextFont_GetLanguageID, _win32_ITextFont_GetLanguageID_cpp, controls.ITextFont_GetLanguageID, controls._win32_ITextFont_GetLanguageID, tom/ITextFont::GetLanguageID
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
 - ITextFont.GetLanguageID
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetLanguageID


## -description


Gets the  language ID or language code identifier (LCID).


## -parameters




### -param pValue

Type: <b>long*</b>

The language ID or LCID. The low word contains the language identifier. The high word is either zero or it contains the high word of the LCID. To retrieve the language identifier, mask out the high word. For more information, see <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale Identifiers</a>. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -remarks



To get the BCP-47 language tag, such as "en-US", call <code>ITextRange2::GetText2(pBstr, tomLanguageTag)</code>, where <i>pBstr</i> specifies the desired language tag. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774167(v=VS.85).aspx">SetLanguageID</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

