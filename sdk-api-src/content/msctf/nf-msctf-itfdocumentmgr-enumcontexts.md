---
UID: NF:msctf.ITfDocumentMgr.EnumContexts
title: ITfDocumentMgr::EnumContexts
author: windows-sdk-content
description: ITfDocumentMgr::EnumContexts method
old-location: tsf\itfdocumentmgr_enumcontexts.htm
tech.root: TSF
ms.assetid: 0656301a-9e24-4b13-bc39-7d9085c0d6f2
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: EnumContexts, EnumContexts method [Text Services Framework], EnumContexts method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],EnumContexts method, ITfDocumentMgr.EnumContexts, ITfDocumentMgr::EnumContexts, _tsf_itfdocumentmgr_enumcontexts_ref, msctf/ITfDocumentMgr::EnumContexts, tsf.itfdocumentmgr_enumcontexts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDocumentMgr.EnumContexts
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfDocumentMgr::EnumContexts


## -description




## -parameters




### -param ppEnum [out]

Address of an <a href="https://msdn.microsoft.com/20b342e6-cac4-4bc5-820b-e397e0ce4648">IEnumTfContexts</a> pointer that receives the enumerator.


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
A memory allocation error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The enumerator cannot be initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/20b342e6-cac4-4bc5-820b-e397e0ce4648">IEnumTfContexts
      </a>



<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a>
 

 

