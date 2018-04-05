---
UID: NF:indexsrv.IStemmer.Init
title: IStemmer::Init method
author: windows-driver-content
description: Initializes the stemmer.
old-location: indexsrv\istemmer_init.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_2a7o.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IStemmer, IStemmer interface [Indexing Service], Init method, IStemmer::Init, Init method [Indexing Service], Init method [Indexing Service], IStemmer interface, Init,IStemmer.Init, _idxs_IStemmer_Init, indexsrv.istemmer_init, indexsrv/IStemmer::Init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WORDREP_BREAK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Indexsrv.h
api_name:
-	IStemmer.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStemmer::Init method


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Initializes the stemmer.


## -parameters




### -param ulMaxTokenSize [in]

The maximum number of characters for words that are added to the WordFormSink. Words that exceed this limit may be truncated. 



### -param pfLicense [out]

Indicates whether there are license restrictions for this <a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a> implementation. <b>TRUE</b> indicates that the stemmer is restricted to authorized use only. <b>FALSE</b> indicates that this implementation can be used freely.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfLicense</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LANGUAGE_E_DATABASE_NOT_FOUND </b></dt>
</dl>
</td>
<td width="60%">
One of the components for word breaking cannot be located.

</td>
</tr>
</table>
 




## -remarks



You must initialize the stemmer. This method is called before any other method of <a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a>. If <i>pfLicense</i> is <b>TRUE</b>, and if you want more information about possible license restrictions, call the <a href="https://msdn.microsoft.com/9d0812a6-679c-4163-aab7-60d0283d7c2c">GetLicenseToUse</a> method.






## -see-also




<a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a>
 

 

