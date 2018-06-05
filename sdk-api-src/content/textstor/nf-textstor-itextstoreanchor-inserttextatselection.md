---
UID: NF:textstor.ITextStoreAnchor.InsertTextAtSelection
title: ITextStoreAnchor::InsertTextAtSelection
author: windows-sdk-content
description: ITextStoreAnchor::InsertTextAtSelection method
old-location: tsf\itextstoreanchor_inserttextatselection.htm
old-project: TSF
ms.assetid: f5cb512a-d9f5-451f-b6cb-2020ba32e855
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],InsertTextAtSelection method, ITextStoreAnchor.InsertTextAtSelection, ITextStoreAnchor::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITextStoreAnchor interface, TF_IAS_NOQUERY, TF_IAS_QUERYONLY, textstor/ITextStoreAnchor::InsertTextAtSelection, tsf.itextstoreanchor_inserttextatselection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreAnchor.InsertTextAtSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchor::InsertTextAtSelection


## -description




## -parameters




### -param dwFlags [in]

Specifies whether the <i>paStart</i> and <i>paEnd</i> parameters will contain the results of the text insertion.

The <a href="https://msdn.microsoft.com/adc5c539-fdb1-4829-ad17-2f54ec179c47">TF_IAS_NOQUERY</a> and TF_IAS_QUERYONLY flags cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NOQUERY"></a><a id="tf_ias_noquery"></a><dl>
<dt><b>TF_IAS_NOQUERY</b></dt>
</dl>
</td>
<td width="60%">
Text is inserted, and the values of the <i>ppaStart</i> and <i>ppaEnd</i> parameters can be <b>NULL</b>. Use this flag if the results of the text insertion are not required.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
Text is not inserted, and the <i>ppaStart</i> and <i>ppaEnd</i> anchors contain the results of the text insertion. The values of these parameters depend on how the application implements text insertion into a document. Use this flag to view the results of the text insertion without actually inserting the text. Zero-length text can be inserted.

</td>
</tr>
</table>
 


### -param pchText [in]

Pointer to the string to insert in the document. The string can be <b>NULL</b> terminated.


### -param cch [in]

Specifies the text length.


### -param ppaStart [out]

Pointer to the anchor object at the start of the text insertion.


### -param ppaEnd [out]

Pointer to the anchor object at the end of the text insertion. For an insertion point, this parameter value will be the same as the value of the <i>ppaStart</i> parameter.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method could not instantiate one of the anchors <i>paStart</i> or <i>paEnd</i>.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/4bdf12bc-c15e-4bdb-8bc0-53172e9c943e">ITextStoreAnchorSink::OnTextChange
      </a>



<a href="https://msdn.microsoft.com/adc5c539-fdb1-4829-ad17-2f54ec179c47">
        TF_IAS_* Constants
      </a>



<a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">
        TS_TEXTCHANGE
      </a>
 

 

