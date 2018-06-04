---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfInsertAtSelection::InsertTextAtSelection


## -description




## -parameters




### -param ec [in]

Identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param dwFlags [in]

Bit field with one of the following values.

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
<i>ppRange</i> is <b>NULL</b>. This flag cannot be combined with the TF_IAS_QUERYONLY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_QUERYONLY"></a><a id="tf_ias_queryonly"></a><dl>
<dt><b>TF_IAS_QUERYONLY</b></dt>
</dl>
</td>
<td width="60%">
The context is not modified, but <i>ppRange</i> is set as if the insert had occurred. Read-only access is sufficient. If this flag is not set, <i>ec</i> must have read/write access. This flag cannot be combined with the TF_IAS_NOQUERY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IAS_NO_DEFAULT_COMPOSITION"></a><a id="tf_ias_no_default_composition"></a><dl>
<dt><b>TF_IAS_NO_DEFAULT_COMPOSITION</b></dt>
</dl>
</td>
<td width="60%">
The manager will not create a default composition if a composition is required. The caller must create a composition object that covers the inserted text before releasing the context lock.

</td>
</tr>
</table>
 


### -param pchText [in]

Specifies the text to insert.


### -param cch [in]

Specifies the character count of the text in <i>pchText</i>.


### -param ppRange [out]

Receives the position of the inserted object.


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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The text service does not have a document lock

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
Context has no selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
Selection is read-only.

</td>
</tr>
</table>
 




## -remarks



To insert an <a href="_ole_idataobject">IDataObject</a> object instead of text, use <a href="https://msdn.microsoft.com/13fa9955-0087-4dd9-8a1d-814ab801e956">ITfInsertAtSelection::InsertEmbeddedAtSelection</a>.




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/bd303639-942f-4cb0-8d69-1715f85b6ef3">
        ITfInsertAtSelection
      </a>



<a href="https://msdn.microsoft.com/13fa9955-0087-4dd9-8a1d-814ab801e956">
        ITfInsertAtSelection::InsertEmbeddedAtSelection
      </a>
 

 

