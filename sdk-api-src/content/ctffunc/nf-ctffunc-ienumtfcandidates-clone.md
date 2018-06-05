---
UID: NF:ctffunc.IEnumTfCandidates.Clone
title: IEnumTfCandidates::Clone
author: windows-sdk-content
description: IEnumTfCandidates::Clone method
old-location: tsf\ienumtfcandidates_clone.htm
old-project: TSF
ms.assetid: 7e7fc6d9-69eb-4457-be28-2b28b9eeeabb
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfCandidates interface, IEnumTfCandidates interface [Text Services Framework],Clone method, IEnumTfCandidates.Clone, IEnumTfCandidates::Clone, _tsf_ienumtfcandidates_clone_ref, ctffunc/IEnumTfCandidates::Clone, tsf.ienumtfcandidates_clone
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	IEnumTfCandidates.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# IEnumTfCandidates::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/4daef7e9-e5ab-4eb8-acb6-a475b84d4de6">IEnumTfCandidates</a> interface pointer that receives the new enumerator.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4daef7e9-e5ab-4eb8-acb6-a475b84d4de6">IEnumTfCandidates
      </a>
 

 

