---
UID: NF:msctf.ITfCandidateListUIElementBehavior.Abort
title: ITfCandidateListUIElementBehavior::Abort (msctf.h)
description: The ITfCandidateListUIElementBehavior::Abort method closes the candidate list. There is no guarantee that the current selection will be finalized.
helpviewer_keywords: ["Abort","Abort method [Text Services Framework]","Abort method [Text Services Framework]","ITfCandidateListUIElementBehavior interface","ITfCandidateListUIElementBehavior interface [Text Services Framework]","Abort method","ITfCandidateListUIElementBehavior.Abort","ITfCandidateListUIElementBehavior::Abort","msctf/ITfCandidateListUIElementBehavior::Abort","tsf.itfcandidatelistuielementbehavior_abort"]
old-location: tsf\itfcandidatelistuielementbehavior_abort.htm
tech.root: TSF
ms.assetid: 2e9d231c-fd80-45fa-bfd0-6a9e057dccf2
ms.date: 12/05/2018
ms.keywords: Abort, Abort method [Text Services Framework], Abort method [Text Services Framework],ITfCandidateListUIElementBehavior interface, ITfCandidateListUIElementBehavior interface [Text Services Framework],Abort method, ITfCandidateListUIElementBehavior.Abort, ITfCandidateListUIElementBehavior::Abort, msctf/ITfCandidateListUIElementBehavior::Abort, tsf.itfcandidatelistuielementbehavior_abort
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCandidateListUIElementBehavior::Abort
 - msctf/ITfCandidateListUIElementBehavior::Abort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfCandidateListUIElementBehavior.Abort
---

# ITfCandidateListUIElementBehavior::Abort


## -description

The <b>ITfCandidateListUIElementBehavior::Abort</b> method closes the candidate list. There is no guarantee that the current selection will be finalized.



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

