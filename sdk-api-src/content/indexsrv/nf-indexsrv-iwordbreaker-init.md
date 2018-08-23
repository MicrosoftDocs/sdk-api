---
UID: NF:indexsrv.IWordBreaker.Init
title: IWordBreaker::Init
author: windows-sdk-content
description: Initializes the IWordBreaker implementation and indicates the mode in which the component operates.
old-location: search\_search_IWordBreaker_Init.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\iwordbreaker\init.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWordBreaker interface [search],Init method, IWordBreaker.Init, IWordBreaker::Init, Init, Init method [search], Init method [search],IWordBreaker interface, _search_IWordBreaker_Init, indexsrv/IWordBreaker::Init, search._search_IWordBreaker_Init
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: indexsrv.h
req.include-header: 
req.redist: Windows NT 4.0 Option Pack
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
 - IWordBreaker.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordBreaker::Init


## -description


Initializes the <a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a> implementation and indicates the mode in which the component operates.


## -parameters




### -param fQuery [in]

Type: <b>BOOL</b>

Flag that indicates the mode in which a word breaker operates. <b>TRUE</b> indicates query-time word breaking. <b>FALSE</b> indicates index-time word breaking.


### -param ulMaxTokenSize [in]

Type: <b>ULONG</b>

Maximum number of characters in words that are added to the <a href="https://msdn.microsoft.com/220FCAE5-D22D-45ED-9689-E78C0D8E0BB3">IWordSink</a>. Words that exceed this limit are truncated.


### -param pfLicense [out]

Type: <b>BOOL*</b>

Pointer to a variable that receives a flag indicating whether there are license restrictions for this <a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a> implementation. <b>TRUE</b> indicates that the stemmer is restricted to authorized use only. <b>FALSE</b> indicates that this <b>IWordBreaker</b> implementation can be used freely.


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
Other errors. 

</td>
</tr>
</table>
 




## -remarks



The functionality of the word breaker is similar in both index creation and querying. Differences are language dependent. If <i>pfLicense</i> is <b>TRUE</b>, and if you want more information about possible license restrictions, call the <a href="https://msdn.microsoft.com/en-us/library/Bb266435(v=VS.85).aspx">IWordBreaker::GetLicenseToUse</a> method.
            




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a>
 

 

