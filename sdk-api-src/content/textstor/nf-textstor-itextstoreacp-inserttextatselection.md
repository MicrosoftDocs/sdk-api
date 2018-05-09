---
UID: NF:textstor.ITextStoreACP.InsertTextAtSelection
title: ITextStoreACP::InsertTextAtSelection
author: windows-driver-content
description: The ITextStoreACP::InsertTextAtSelection method inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.
old-location: tsf\itextstoreacp_inserttextatselection.htm
old-project: TSF
ms.assetid: b57ad8da-6f79-4d27-96e0-608cbcaae826
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: 0, ITextStoreACP interface [Text Services Framework],InsertTextAtSelection method, ITextStoreACP.InsertTextAtSelection, ITextStoreACP::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITextStoreACP interface, TF_IAS_NOQUERY, TF_IAS_QUERYONLY, _tsf_itextstoreacp_inserttextatselection_ref, acpNewEnd, acpOldEnd, acpStart, textstor/ITextStoreACP::InsertTextAtSelection, tsf.itextstoreacp_inserttextatselection
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ITextStoreACP.InsertTextAtSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::InsertTextAtSelection


## -description


The <b>ITextStoreACP::InsertTextAtSelection</b> method inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.


## -parameters




### -param dwFlags [in]

Specifies whether the <i>pacpStart</i> and <i>pacpEnd</i> parameters and the <a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE</a> structure contain the results of the text insertion.

The <a href="https://msdn.microsoft.com/adc5c539-fdb1-4829-ad17-2f54ec179c47">TF_IAS_NOQUERY</a> and TF_IAS_QUERYONLY flags cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Text insertion will occur, and the <i>pacpStart</i> and <i>pacpEnd</i> parameters will contain the results of the text insertion. The <b>TS_TEXTCHANGE</b> structure must be filled with this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NOQUERY"></a><a id="tf_ias_noquery"></a><dl>
<dt><b>TF_IAS_NOQUERY</b></dt>
</dl>
</td>
<td width="60%">
Text is inserted, the values of the <i>pacpStart</i> and <i>pacpEnd</i> parameters can be <b>NULL</b>, and the <b>TS_TEXTCHANGE</b> structure must be filled. Use this flag to view the results of the text insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
Text is not inserted, and the values for the <i>pacpStart</i> and <i>pacpEnd</i> parameters contain the results of the text insertion. The values of these parameters depend on how the application implements text insertion into a document. For more information, see the Remarks section. Use this flag to view the results of the text insertion without actually inserting the text. It is not required that you fill the <b>TS_TEXTCHANGE</b> structure if you use this flag.

</td>
</tr>
</table>
 


### -param pchText [in]

Pointer to the string to insert in the document. The string can be <b>NULL</b> terminated.


### -param cch [in]

Specifies the text length.


### -param pacpStart [out]

Pointer to the starting application character position where the text insertion occurs.


### -param pacpEnd [out]

Pointer to the ending application character position where the text insertion occurs. This parameter value is the same as the value of the <i>pacpStart</i> parameter for an insertion point.


### -param pChange [out]

Pointer to a <b>TS_TEXTCHANGE</b> structure with the following members.

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
The ending application character position before the text is inserted into the document. This value is the same as <b>acpStart</b> for an insertion point. If this value is different from <b>acpStart</b>, then text was selected prior to the text insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="acpNewEnd"></a><a id="acpnewend"></a><a id="ACPNEWEND"></a><dl>
<dt><b>acpNewEnd</b></dt>
</dl>
</td>
<td width="60%">
The end position after the text insertion occurred.

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
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a lock on the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pchText</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



The values of the <i>pacpStart</i> and the <i>pacpEnd</i> parameters depend upon how the client application inserts text into a document. For example, if the application sets the cursor at the start of the inserted text after text insertion, then the value for the <i>pacpStart</i> and <i>pacpEnd</i> parameters is the same as the <b>acpStart</b> member of the <b>TS_TEXTCHANGE</b> structure.

Applications should not call the <a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">ITextStoreACPSink::OnTextChange</a> method in response to this method.




## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">ITextStoreACPSink::OnTextChange
      </a>



<a href="https://msdn.microsoft.com/adc5c539-fdb1-4829-ad17-2f54ec179c47">
        TF_IAS_* Constants
      </a>



<a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">
        TS_TEXTCHANGE
      </a>
 

 

