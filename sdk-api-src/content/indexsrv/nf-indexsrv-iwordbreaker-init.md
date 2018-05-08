---
UID: NF:indexsrv.IWordBreaker.Init
title: IWordBreaker::Init
author: windows-driver-content
description: Initializes the IWordBreaker implementation and indicates the mode in which the component operates.
old-location: indexsrv\iwordbreaker_init.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_18ac.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWordBreaker interface [Indexing Service],Init method, IWordBreaker.Init, IWordBreaker::Init, Init, Init method [Indexing Service], Init method [Indexing Service],IWordBreaker interface, _idxs_IWordBreaker_Init, indexsrv.iwordbreaker_init, indexsrv/IWordBreaker::Init
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
-	IWordBreaker.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordBreaker::Init


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Initializes the <a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> implementation and indicates the mode in which the component operates.


## -parameters




### -param fQuery [in]

Indicates the mode in which a word breaker operates. <b>TRUE</b> indicates query-time word breaking. <b>FALSE</b> indicates index-time word breaking. 



### -param ulMaxTokenSize [in]

The maximum number of characters in words that are added to the WordSink. Words that exceed this limit may be truncated. 


### -param pfLicense [out]

A pointer to an output variable that receives a value that indicates whether there are license restrictions for this <a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> implementation. <b>TRUE</b> indicates that the stemmer is restricted to authorized use only. <b>FALSE</b> indicates that this implementation can be used freely.


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



The functionality of the word breaker is similar in both index creation and querying. Differences are language dependent. If <i>pfLicense</i> is <b>TRUE</b>, and if you want more information about possible license restrictions, call the <a href="https://msdn.microsoft.com/e79b017d-ca88-4e4d-b3d1-b1c046143e86">GetLicenseToUse</a> method.






## -see-also




<a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a>
 

 

