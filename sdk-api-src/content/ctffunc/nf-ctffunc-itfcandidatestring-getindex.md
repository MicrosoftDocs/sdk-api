---
UID: NF:ctffunc.ITfCandidateString.GetIndex
title: ITfCandidateString::GetIndex
author: windows-sdk-content
description: ITfCandidateString::GetIndex method
old-location: tsf\itfcandidatestring_getindex.htm
old-project: TSF
ms.assetid: 16ec9a89-db57-41ad-9e32-db0b24abda13
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetIndex, GetIndex method [Text Services Framework], GetIndex method [Text Services Framework],ITfCandidateString interface, ITfCandidateString interface [Text Services Framework],GetIndex method, ITfCandidateString.GetIndex, ITfCandidateString::GetIndex, _tsf_itfcandidatestring_getindex_ref, ctffunc/ITfCandidateString::GetIndex, tsf.itfcandidatestring_getindex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tiptsf.dll
api_name:
 - ITfCandidateString.GetIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
---

# ITfCandidateString::GetIndex


## -description




## -parameters




### -param pnIndex [out]

Pointer to a <b>ULONG</b> value that receives the zero-based index of the candidate string object within the candidate list.


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
<i>pnIndex</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e41ba461-6337-4feb-ba16-3942920ebb9f">
        ITfCandidateList
      </a>



<a href="https://msdn.microsoft.com/82c77b59-a50c-42ae-ba1d-25a1c196662d">ITfCandidateString</a>
 

 

