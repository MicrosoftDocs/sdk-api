---
UID: NF:msctf.ITfThreadMgr2.Deactivate
title: ITfThreadMgr2::Deactivate (msctf.h)
author: windows-sdk-content
description: Deactivates TSF for the calling thread.
old-location: tsf\itfthreadmgr2_deactivate.htm
tech.root: TSF
ms.assetid: 5ED1A430-27C3-44BA-BF17-B5FB9D4C7087
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Deactivate, Deactivate method [Text Services Framework], Deactivate method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],Deactivate method, ITfThreadMgr2.Deactivate, ITfThreadMgr2::Deactivate, msctf/ITfThreadMgr2::Deactivate, tsf.itfthreadmgr2_deactivate
ms.topic: method
f1_keywords: 
 - "msctf/ITfThreadMgr2.Deactivate"
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.Deactivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfThreadMgr2::Deactivate


## -description


Deactivates TSF for the calling thread.


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
This method was called while the thread was activated or this call had no corresponding <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-activate">Activate</a> call.

</td>
</tr>
</table>
 




## -remarks



Each call to this method must be matched with a previous call to <b>Activate</b>. This method must be called from the same thread that the corresponding <b>Activate</b> call was made from.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>
 

 

