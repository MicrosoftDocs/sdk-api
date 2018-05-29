---
UID: NF:textstor.ITextStoreACP.SetText
title: ITextStoreACP::SetText
author: windows-sdk-content
description: The ITextStoreACP::SetText method sets the text selection to the supplied character positions.
old-location: tsf\itextstoreacp_settext.htm
old-project: TSF
ms.assetid: aebeb6bc-7791-4c45-8563-eec6a738bd63
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],SetText method, ITextStoreACP.SetText, ITextStoreACP::SetText, SetText, SetText method [Text Services Framework], SetText method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_settext_ref, acpNewEnd, acpOldEnd, acpStart, textstor/ITextStoreACP::SetText, tsf.itextstoreacp_settext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.SetText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::SetText


## -description


The <b>ITextStoreACP::SetText</b> method sets the text selection to the supplied character positions.


## -parameters




### -param dwFlags [in]

If set to the value of TS_ST_CORRECTION, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. The client defines the type of markup information to be retained.


### -param acpStart [in]

Specifies the starting character position of the text to replace.


### -param acpEnd [in]

Specifies the ending character position of the text to replace. This parameter is ignored if the value is 1.


### -param pchText [in]

Specifies the pointer to the replacement text. The text string does not have to be <b>NULL</b> terminated, because the text character count is specified in the <i>cch</i> parameter.


### -param cch [in]

Specifies the number of characters in the replacement text.


### -param pChange [out]

Pointer to a <a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE</a> structure with the following data.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="acpStart"></a><a id="acpstart"></a><a id="ACPSTART"></a><dl>
<dt><b>acpStart</b></dt>
</dl>
</td>
<td width="60%">
The starting application character position before the text is inserted into the document.

</td>
</tr>
<tr>
<td width="40%"><a id="acpOldEnd"></a><a id="acpoldend"></a><a id="ACPOLDEND"></a><dl>
<dt><b>acpOldEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending position before the text is inserted into the document. This value is the same as <i>acpStart</i> for an insertion point. If this value is different from <i>acpStart</i>, then text was selected prior to the text insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="acpNewEnd"></a><a id="acpnewend"></a><a id="ACPNEWEND"></a><dl>
<dt><b>acpNewEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending position after the text insertion occurred.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The <i>acpStart</i> or <i>acpEnd</i> parameter is outside of the document text.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The document is read-only. Content cannot be modified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_REGION</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to modify text across a region boundary.

</td>
</tr>
</table>
 




## -remarks



Applications should start a composition by first using <a href="https://msdn.microsoft.com/b57ad8da-6f79-4d27-96e0-608cbcaae826">ITextStoreACP::InsertTextAtSelection</a>. <b>ITextStoreACP::SetText</b> should be used only within an existing composition. If there is no active composition at the time <b>SetText</b> is called, the TSF manager creates a composition that lasts just long enough to wrap the call to <b>SetText</b>.

The <i>acpStart</i> and <i>acpEnd</i> character positions cannot be outside the document range.

Applications should not call the <a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">ITextStoreACPSink::OnTextChange</a> method in response to this method.

This method should call the <a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">ITextStoreACP::SetSelection</a> method to select the text to be changed. After successfully executing the <b>ITextStoreACP::SetSelection</b> method, this method then calls the <b>ITextStoreACP::InsertTextAtSelection</b> method to perform the actual text change.




## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">ITextStoreACPSink::OnTextChange
      </a>



<a href="https://msdn.microsoft.com/6e05ed74-fff3-4bc4-a21e-9af9492af23b">
        Miscellaneous Text Store Constants
      </a>



<a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">
        TS_TEXTCHANGE
      </a>
 

 

