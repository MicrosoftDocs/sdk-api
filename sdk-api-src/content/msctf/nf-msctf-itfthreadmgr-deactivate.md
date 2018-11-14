---
UID: NF:msctf.ITfThreadMgr.Deactivate
title: ITfThreadMgr::Deactivate
author: windows-sdk-content
description: ITfThreadMgr::Deactivate method
old-location: tsf\itfthreadmgr_deactivate.htm
tech.root: TSF
ms.assetid: 7293fbfa-c385-4713-80b2-760e54dbf4c1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Deactivate, Deactivate method [Text Services Framework], Deactivate method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],Deactivate method, ITfThreadMgr.Deactivate, ITfThreadMgr::Deactivate, _tsf_itfthreadmgr_deactivate_ref, msctf/ITfThreadMgr::Deactivate, tsf.itfthreadmgr_deactivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Msctf.dll
api_name:
 - ITfThreadMgr.Deactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfThreadMgr.Deactivate
: 
---

# ITfThreadMgr::Deactivate


## -description




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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called while the thread was activating or this call had no corresponding <a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate</a> call.

</td>
</tr>
</table>
 




## -remarks



Each call to this method must be matched with a previous call to <b>ITfThreadMgr::Activate</b> . This method must be called from the same thread that the corresponding <b>ITfThreadMgr::Activate</b> call was made from.




## -see-also




<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>



<a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate
      </a>
 

 

