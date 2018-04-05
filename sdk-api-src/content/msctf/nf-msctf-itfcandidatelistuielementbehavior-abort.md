---
UID: NF:msctf.ITfCandidateListUIElementBehavior.Abort
title: ITfCandidateListUIElementBehavior::Abort method
author: windows-driver-content
description: The ITfCandidateListUIElementBehavior::Abort method closes the candidate list. There is no guarantee that the current selection will be finalized.
old-location: tsf\itfcandidatelistuielementbehavior_abort.htm
old-project: TSF
ms.assetid: 2e9d231c-fd80-45fa-bfd0-6a9e057dccf2
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: Abort method [Text Services Framework], Abort method [Text Services Framework], ITfCandidateListUIElementBehavior interface, Abort,ITfCandidateListUIElementBehavior.Abort, ITfCandidateListUIElementBehavior, ITfCandidateListUIElementBehavior interface [Text Services Framework], Abort method, ITfCandidateListUIElementBehavior::Abort, msctf/ITfCandidateListUIElementBehavior::Abort, tsf.itfcandidatelistuielementbehavior_abort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfCandidateListUIElementBehavior.Abort
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCandidateListUIElementBehavior::Abort method


## -description


The <b>ITfCandidateListUIElementBehavior::Abort</b> method closes the candidate list. There is no guarantee that the current selection will be finalized.


## -parameters






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
 



