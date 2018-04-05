---
UID: NF:tom.ITextFont.SetLanguageID
title: ITextFont::SetLanguageID method
author: windows-driver-content
description: Sets the language ID or language code identifier (LCID).
old-location: controls\ITextFont_SetLanguageID.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setlanguageid.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], SetLanguageID method, ITextFont::SetLanguageID, SetLanguageID method [Windows Controls], SetLanguageID method [Windows Controls], ITextFont interface, SetLanguageID,ITextFont.SetLanguageID, _win32_ITextFont_SetLanguageID, _win32_ITextFont_SetLanguageID_cpp, controls.ITextFont_SetLanguageID, controls._win32_ITextFont_SetLanguageID, tom/ITextFont::SetLanguageID
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont.SetLanguageID
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::SetLanguageID method


## -description


Sets the  language ID or language code identifier (LCID).


## -parameters




### -param Value [in]

Type: <b>long</b>

The new language identifier. The low word contains the language identifier. The high word is either zero or it contains the high word of the locale identifier LCID. For more information, see <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale Identifiers</a>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



If the high nibble of  <i>Value</i> is <a href="tomconstants.htm">tomCharset</a>, set the <i>charrep</i> from the <i>charset</i> in the low byte and the pitch and family from the next byte. See also <a href="https://msdn.microsoft.com/6c57b5e5-a5c7-416a-851c-fc8ef16b5a9a">ITextFont2::SetCharRep</a>. 

If the high nibble of <i>Value</i> is <a href="tomconstants.htm">tomCharRepFromLcid</a>, set the <i>charrep</i> from the LCID and set the LCID as well. See <a href="https://msdn.microsoft.com/422f94bc-44ef-44db-be8c-50fe1acc2320">ITextFont::GetLanguageID</a> for more information. 


To set the BCP-47 language tag, such as "en-US", call <a href="https://msdn.microsoft.com/dd7a8a16-6cb5-40ee-8f5f-e51e68785d93">ITextRange2::SetText2</a> and set the <a href="tomconstants.htm">tomLanguageTag</a> and <i>bstr</i> with the language tag.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/422f94bc-44ef-44db-be8c-50fe1acc2320">GetLanguageID</a>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

