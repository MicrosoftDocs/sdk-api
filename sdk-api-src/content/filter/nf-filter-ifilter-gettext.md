---
UID: NF:filter.IFilter.GetText
title: IFilter::GetText
author: windows-sdk-content
description: Retrieves text (text-type properties) from the current chunk, which must have a CHUNKSTATE enumeration value of CHUNK_TEXT.
old-location: indexsrv\ifilter_gettext.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_5378.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetText, GetText method [Indexing Service], GetText method [Indexing Service],IFilter interface, IFilter interface [Indexing Service],GetText method, IFilter.GetText, IFilter::GetText, _idxs_IFilter_GetText, filter/IFilter::GetText, indexsrv.ifilter_gettext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: filter.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: IFILTER_INIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Filter.h
api_name:
 - IFilter.GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFilter::GetText


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Retrieves text (text-type properties) from the current chunk, which must have a <a href="https://msdn.microsoft.com/67a39a45-faca-4aad-8d9c-5ee0525a59e7">CHUNKSTATE</a> enumeration value of CHUNK_TEXT.



## -parameters




### -param pcwcBuffer [in, out]

On entry, the size of <i>awcBuffer</i> array in wide/Unicode characters. On exit, the number of Unicode characters written to <i>awcBuffer</i>.


### -param awcBuffer [out]

Text retrieved from the current chunk. Do not terminate the buffer with a character. Use a null-terminated string. The null-terminated string should not exceed the size of the destination buffer. 



## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_NO_TEXT 
</b></dt>
</dl>
</td>
<td width="60%">
The <b>flags</b> member of the <a href="https://msdn.microsoft.com/fb3e432d-3c8b-4567-9dc3-c35961f100ff">STAT_CHUNK</a> structure for the current chunk does not have a value of CHUNK_TEXT. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_NO_MORE_TEXT </b></dt>
</dl>
</td>
<td width="60%">
All the text in the current chunk has been returned. Additional calls to the <a href="https://msdn.microsoft.com/d63639a6-6729-44cd-8105-198a268ff2d6">GetText</a> method should return this error until the <a href="https://msdn.microsoft.com/4d4f3150-deec-40b6-a945-b4cea241db8d">IFilter::GetChunk</a> method has been called successfully. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_S_LAST_TEXT </b></dt>
</dl>
</td>
<td width="60%">
As an optimization, the last call that returns text can return FILTER_S_LAST_TEXT, indicating that the next call to the <a href="https://msdn.microsoft.com/d63639a6-6729-44cd-8105-198a268ff2d6">GetText</a> method will return FILTER_E_NO_MORE_TEXT. This optimization can save time by eliminating unnecessary calls to <b>GetText</b>.

</td>
</tr>
</table>
 




## -remarks



If the current chunk is too large for the <i>awcBuffer</i> array, more than one call to the <b>GetText</b> method can be required to retrieve all the text in the current chunk. Each call to the <b>GetText</b> method retrieves text that immediately follows the text from the last call to the <b>GetText</b> method. The last character from one call can be in the middle of a word, and the first character in the next call would continue that word. Search engines must handle this situation.






## -see-also




<a href="https://msdn.microsoft.com/67a39a45-faca-4aad-8d9c-5ee0525a59e7">CHUNKSTATE</a>



<a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a>
 

 

