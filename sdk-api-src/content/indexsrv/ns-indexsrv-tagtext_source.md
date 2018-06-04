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

# tagTEXT_SOURCE structure


## -description


Contains information about text that the word breaker will process.


## -struct-fields




### -field pfnFillTextBuffer

Type: <b>PFNFILLTEXTBUFFER</b>

Pointer to a function, <b>PFNFILLTEXTBUFFER</b> that refills the <b>awcBuffer</b> with text from the source document.


### -field awcBuffer

Type: <b>WCHAR*</b>

Pointer to a buffer that contains text from the source document for the word breaker to parse.


### -field iEnd

Type: <b>ULONG</b>

Position of the last character in <b>awcBuffer</b>.


### -field iCur

Type: <b>ULONG</b>

Position of the first character in <b>awcBuffer</b>.


## -remarks



Windows Search populates the members of this structure when the word breaker is invoked and initialized. <a href="https://msdn.microsoft.com/32e495c0-e173-4b35-be58-51f31cb38e3e">IWordBreaker::BreakText</a> gets a pointer to a <b>TEXT_SOURCE</b> structure and calls PFNFILLTEXTBUFFER, the function pointed to by the <b>pfnFillTextBuffer</b> member, to refill <b>awcBuffer</b> until all text from the source is processed. The <b>PFNFILLTEXTBUFFER</b> function returns an <b>HRESULT</b> that includes both filtering and word-breaking return values.

 
                The filtering return values are the following:

<ul>
<li>FILTER_E_NO_MORE_VALUES</li>
<li>FILTER_E_NO_TEXT</li>
<li>FILTER_E_NO_VALUES</li>
<li>FILTER_E_NO_MORE_TEXT</li>
<li>FILTER_E_END_OF_CHUNKS</li>
</ul>
For more information about these return values, see <a href="_idxs_filter_interface_values">Filter-Interface Values</a>.

The word-breaking return value is WBREAK_E_END_OF_TEXT. For more information about word-breaking return values, see <a href="_idxs_word_breaking_values">Word-Breaking Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/32e495c0-e173-4b35-be58-51f31cb38e3e">IWordBreaker::BreakText</a>
 

 

