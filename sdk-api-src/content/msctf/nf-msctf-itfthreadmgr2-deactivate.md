---
UID: NF:msctf.ITfThreadMgr2.Deactivate
title: ITfThreadMgr2::Deactivate
author: windows-sdk-content
description: Deactivates TSF for the calling thread.
old-location: tsf\itfthreadmgr2_deactivate.htm
old-project: TSF
ms.assetid: 5ED1A430-27C3-44BA-BF17-B5FB9D4C7087
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Deactivate, Deactivate method [Text Services Framework], Deactivate method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],Deactivate method, ITfThreadMgr2.Deactivate, ITfThreadMgr2::Deactivate, msctf/ITfThreadMgr2::Deactivate, tsf.itfthreadmgr2_deactivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.Deactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
This method was called while the thread was activated or this call had no corresponding <a href="https://msdn.microsoft.com/FD1548F5-15F6-4BBC-A7D1-B0F4B881D9F8">Activate</a> call.

</td>
</tr>
</table>
 




## -remarks



Each call to this method must be matched with a previous call to <b>Activate</b>. This method must be called from the same thread that the corresponding <b>Activate</b> call was made from.




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

