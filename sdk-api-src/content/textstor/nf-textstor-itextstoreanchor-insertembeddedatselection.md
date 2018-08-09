---
UID: NF:textstor.ITextStoreAnchor.InsertEmbeddedAtSelection
title: ITextStoreAnchor::InsertEmbeddedAtSelection
author: windows-sdk-content
description: The ITextStoreAnchor::InsertEmbeddedAtSelection method inserts an IDataObject object at the insertion point or selection. The client that calls this method must have a read/write lock before inserting an IDataObject into the text stream.
old-location: tsf\itextstoreanchor_insertembeddedatselection.htm
old-project: TSF
ms.assetid: 22c804b9-e260-4a8a-bbb3-fcc81fa97c7a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],InsertEmbeddedAtSelection method, ITextStoreAnchor.InsertEmbeddedAtSelection, ITextStoreAnchor::InsertEmbeddedAtSelection, InsertEmbeddedAtSelection, InsertEmbeddedAtSelection method [Text Services Framework], InsertEmbeddedAtSelection method [Text Services Framework],ITextStoreAnchor interface, TF_IAS_NOQUERY, TF_IAS_QUERYONLY, textstor/ITextStoreAnchor::InsertEmbeddedAtSelection, tsf.itextstoreanchor_insertembeddedatselection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.InsertEmbeddedAtSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchor::InsertEmbeddedAtSelection


## -description


The <b>ITextStoreAnchor::InsertEmbeddedAtSelection</b> method inserts an <a href="_ole_idataobject">IDataObject</a> object at the insertion point or selection. The client that calls this method must have a read/write lock before inserting an <b>IDataObject</b> into the text stream.


## -parameters




### -param dwFlags [in]

Specifies whether the <i>paStart</i> and <i>paEnd</i> parameters will contain the results of the object insertion.

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
Text is not inserted, and the <i>ppaStart</i> and <i>ppaEnd</i> anchors contain the results of the text insertion. The values of these parameters depend on how the application implements text insertion into a document.

Use this flag to view the results of the text insertion without actually inserting the text, for example, to predict the results of collapsing or otherwise adjusting a selection.

</td>
</tr>
</table>
 


### -param pDataObject [in]

Pointer to the <b>IDataObject</b> object to be inserted.


### -param ppaStart [out]

Pointer to the anchor object at the start of the object insertion.


### -param ppaEnd [out]

Pointer to the anchor object at the end of the object insertion. For an insertion point, this parameter value will be the same as the value of the <i>ppaStart</i> parameter.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not instantiate one of the anchors <i>paStart</i> or <i>paEnd</i>.

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
 




## -remarks



Clients must use this method to insert an object into a text stream, since a <a href="https://msdn.microsoft.com/b40ca931-d45c-4101-9380-bb2b3ad25fba">TS_CHAR_EMBEDDED</a> constant cannot be passed into <a href="https://msdn.microsoft.com/03beac03-cd09-4e03-b700-d96741e4932b">ITextStoreAnchor::SetText</a>.




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/722506fa-db83-49d3-9434-a4ad7b797ce2">ITextStoreAnchor::QueryInsertEmbedded
      </a>



<a href="https://msdn.microsoft.com/03beac03-cd09-4e03-b700-d96741e4932b">ITextStoreAnchor::SetText
      </a>



<a href="https://msdn.microsoft.com/adc5c539-fdb1-4829-ad17-2f54ec179c47">TF_IAS_* Constants
      </a>



<a href="https://msdn.microsoft.com/b40ca931-d45c-4101-9380-bb2b3ad25fba">TS_CHAR_EMBEDDED
      </a>
 

 

