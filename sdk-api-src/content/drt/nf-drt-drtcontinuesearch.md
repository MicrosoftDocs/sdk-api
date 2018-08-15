---
UID: NF:drt.DrtContinueSearch
title: DrtContinueSearch function
author: windows-sdk-content
description: DrtContinueSearch function continues an iterative search for a key.
old-location: p2p\drtcontinuesearch.htm
old-project: p2psdk
ms.assetid: 04bdeb53-4901-41d4-835e-da665095edc5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrtContinueSearch, DrtContinueSearch function [Peer Networking], drt/DrtContinueSearch, p2p.drtcontinuesearch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: drt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtContinueSearch
product: Windows
targetos: Windows
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
---

# DrtContinueSearch function


## -description


The <b>DrtContinueSearch</b> function continues an iterative search for a key.This function is used only when the <b>fIterative</b> flag is set to 'true' in the associated <a href="https://msdn.microsoft.com/a3f12d8a-95ef-4168-8d2d-c317ae2c57b4">DRT_SEARCH_INFO</a> structure. Call this after getting a <b>DRT_MATCH_INTERMEDIATE</b> search result.


## -parameters




### -param hSearchContext [in]

Handle to the search context  to close. This parameter is returned by the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> API.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hSearchContext</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This search is not an iterative search.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a3f12d8a-95ef-4168-8d2d-c317ae2c57b4">DRT_SEARCH_INFO</a>



<a href="https://msdn.microsoft.com/1a99476f-69ee-4aeb-8c9b-e06315ec095d">DrtEndSearch</a>



<a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a>
 

 

