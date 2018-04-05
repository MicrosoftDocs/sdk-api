---
UID: NS:indexsrv.tagTEXT_SOURCE
title: tagTEXT_SOURCE
author: windows-driver-content
description: Contains information about text for the word breaker to process.
old-location: indexsrv\text_source.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_13xh.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: TEXT_SOURCE, TEXT_SOURCE structure [Indexing Service], _idxs_TEXT_SOURCE, indexsrv.text_source, indexsrv/TEXT_SOURCE, tagTEXT_SOURCE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TEXT_SOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Indexsrv.h
api_name:
-	TEXT_SOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagTEXT_SOURCE structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Contains information about text for the word breaker to process.



## -struct-fields




### -field pfnFillTextBuffer

A pointer to a function of type <b>PFNFILLTEXTBUFFER</b>. This function refills the <b>awcBuffer</b> member with text from the source document. 



### -field awcBuffer

A pointer to a buffer that contains text from the source document for the word breaker to parse.


### -field iEnd

The position of the last character in <b>awcBuffer</b>.


### -field iCur

The position of the first character in <b>awcBuffer</b>.


## -remarks



The syntax of the <b>pfnFillTextBuffer</b> function is as follows.

<pre class="syntax" xml:space="preserve"><code>typedef HRESULT ( __stdcall *PFNFILLTEXTBUFFER )( 
    struct tagTEXT_SOURCE *pTextSource);
</code></pre>
Indexing Service populates elements of this structure when the word breaker is invoked and initialized. <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">IWordBreaker::BreakText</a> gets a pointer to <b>TEXT_SOURCE</b> structure and calls the function pointed to by the <b>pfnFillTextBuffer</b> parameter, to refill the <b>awcBuffer</b> member until all text from the source has been processed.

The <b>PFNFILLTEXTBUFFER</b> function returns an <b>HRESULT</b> value that includes both filtering and word-breaking return values. The filtering return values are FILTER_E_NO_MORE_VALUES, FILTER_E_NO_TEXT, FILTER_E_NO_VALUES, FILTER_E_NO_MORE_TEXT, and FILTER_E_END_OF_CHUNKS. For more information, see <a href="https://msdn.microsoft.com/a9f94b0d-f3d0-4cf1-9dfe-74c938601abc">Filter-Interface Values</a>. The word-breaking return value is WBREAK_E_END_OF_TEXT. For more information about word-breaking return values, see <a href="https://msdn.microsoft.com/85af046e-c809-47bc-9646-bd1584cd8e66">Word-Breaking Values</a>.






## -see-also




<a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">IWordBreaker::BreakText</a>
 

 

