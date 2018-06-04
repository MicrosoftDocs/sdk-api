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

# ITfInsertAtSelection::InsertEmbeddedAtSelection


## -description


The <b>ITfInsertAtSelection::InsertEmbeddedAtSelection</b> method inserts an <a href="_ole_idataobject">IDataObject</a> object at the selection or insertion point.


## -parameters




### -param ec [in]

Identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param dwFlags [in]

Bit field with one of the following values:

TF_IAS_NOQUERY

The <i>ppRange</i> parameter is <b>NULL</b> on exit.

TF_IAS_QUERYONLY

Context is not modified but the <i>ppRange</i> parameter is set as if the insert occurred. Read-only access is sufficient. If this flag is not set, the <i>ec</i> parameter must have read/write access.

TF_IAS_NO_DEFAULT_COMPOSITION

The TSF manager does not create a default composition if a composition is required. The caller must create a composition object that covers the inserted text before releasing the context lock.


### -param pDataObject [in]

Pointer to object to insert.


### -param ppRange [out]

Position of the inserted object. Optional.


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
The <i>ec</i> parameter is an invalid edit cookie.

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
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Context owner cannot handle objects of the type provided by the <i>pDataObject</i> parameter.

</td>
</tr>
</table>
 




## -remarks



Callers can use the <a href="https://msdn.microsoft.com/52f9465f-725e-493b-89ee-1b3db3cef696">ITfQueryEmbedded::QueryInsertEmbedded</a> method to determine if a particular object type is likely to be accepted by this method.

To insert text instead of an <b>IDataObject</b> object, use the <a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">ITfInsertAtSelection::InsertTextAtSelection</a> method.




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">
        ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/bd303639-942f-4cb0-8d69-1715f85b6ef3">ITfInsertAtSelection
      </a>



<a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">
        ITfInsertAtSelection::InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/52f9465f-725e-493b-89ee-1b3db3cef696">
        ITfQueryEmbedded::QueryInsertEmbedded
      </a>
 

 

