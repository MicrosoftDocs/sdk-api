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

# ITextStoreACPSink::OnTextChange


## -description




## -parameters




### -param dwFlags [in]

Contains a set of flags that specify additional information about the text change. This can be one or more of the following values.

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
The text has changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ST_CORRECTION"></a><a id="ts_st_correction"></a><dl>
<dt><b>TS_ST_CORRECTION</b></dt>
</dl>
</td>
<td width="60%">
The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. This flag is used for applications that need to preserve data associated with the original text.

</td>
</tr>
</table>
 


### -param pChange [in]

Pointer to a <a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE</a> structure that contains text change data.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pChange</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The TSF manager holds a lock on the document. This typically indicates that the method was called from within another <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> method, such as <a href="https://msdn.microsoft.com/aebeb6bc-7791-4c45-8563-eec6a738bd63">ITextStoreACP::SetText</a>.

</td>
</tr>
</table>
 




## -remarks



<b>ITextStoreACPSink::OnTextChange</b> is never called when the text is modified by one of the <b>ITextStoreACP</b> interface methods, such as <b>ITextStoreACP::SetText</b> or <a href="https://msdn.microsoft.com/b57ad8da-6f79-4d27-96e0-608cbcaae826">ITextStoreACP::InsertTextAtSelection</a>.

When calling this method, the application must be able to grant a <a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">document lock</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">
        ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/b57ad8da-6f79-4d27-96e0-608cbcaae826">
        ITextStoreACP::InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/ddd2b1f4-47de-4e87-be94-eea694ecd1b8">
        ITextStoreACP::RequestLock
      </a>



<a href="https://msdn.microsoft.com/aebeb6bc-7791-4c45-8563-eec6a738bd63">
        ITextStoreACP::SetText
      </a>



<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>



<a href="https://msdn.microsoft.com/6e05ed74-fff3-4bc4-a21e-9af9492af23b">
        Miscellaneous Text Store Constants
      </a>



<a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE
      </a>
 

 

