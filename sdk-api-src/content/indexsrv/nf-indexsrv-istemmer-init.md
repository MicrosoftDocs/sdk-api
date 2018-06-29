---
UID: NF:indexsrv.IStemmer.Init
title: IStemmer::Init
author: windows-sdk-content
description: Initializes the stemmer.
old-location: search\_search_IStemmer_Init.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\istemmer\init.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IStemmer interface [search],Init method, IStemmer.Init, IStemmer::Init, Init, Init method [search], Init method [search],IStemmer interface, _search_IStemmer_Init, indexsrv/IStemmer::Init, search._search_IStemmer_Init
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WORDREP_BREAK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Indexsrv.h
api_name:
 - IStemmer.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStemmer::Init


## -description


Initializes the stemmer.


## -parameters




### -param ulMaxTokenSize [in]

Type: <b>ULONG</b>

Maximum number of characters for words that are added to the <a href="https://msdn.microsoft.com/81D52B0C-BADD-48C0-85DB-57CA82D7BBA8">IWordFormSink</a> object. Words that exceed this limit may be truncated.


### -param pfLicense [out]

Type: <b>BOOL</b>

Pointer to an output variable that receives a flag that indicates whether there are license restrictions for this <a href="https://msdn.microsoft.com/library/Bb266437(v=VS.85).aspx">IStemmer</a> implementation. <b>TRUE</b> indicates that the stemmer is restricted to authorized use only. <b>FALSE</b> indicates that this <b>IStemmer</b> implementation can be used freely.


## -returns



Type: <b>HRESULT</b>

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
Successful completion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LANGUAGE_E_DATABASE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
One of the components for word breaking cannot be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. The <i>pfLicense</i> parameter is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unsuccessful completion.

</td>
</tr>
</table>
 




## -remarks



You must initialize the stemmer. The <b>IStemmer::Init</b> method must be called before any other method of <a href="https://msdn.microsoft.com/library/Bb266437(v=VS.85).aspx">IStemmer</a>. If <i>pfLicense</i> is <b>TRUE</b>, and you want more information about possible license restrictions, call the <a href="https://msdn.microsoft.com/library/Bb266435(v=VS.85).aspx">IStemmer::GetLicenseToUse</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb266437(v=VS.85).aspx">IStemmer</a>
 

 

