---
UID: NF:msctf.ITfThreadMgr2.Activate
title: ITfThreadMgr2::Activate
author: windows-sdk-content
description: Activates TSF for the calling thread.
old-location: tsf\itfthreadmgr2_activate.htm
tech.root: TSF
ms.assetid: FD1548F5-15F6-4BBC-A7D1-B0F4B881D9F8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Activate, Activate method [Text Services Framework], Activate method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],Activate method, ITfThreadMgr2.Activate, ITfThreadMgr2::Activate, msctf/ITfThreadMgr2::Activate, tsf.itfthreadmgr2_activate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITfThreadMgr2.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfThreadMgr2::Activate


## -description


 Activates TSF for the calling thread.


## -parameters




### -param ptid [out]

Pointer to a <a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId</a> value that receives a client identifier.


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
<i>ptid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called while the thread was deactivated.

</td>
</tr>
</table>
 




## -remarks



This method can be called more than once from a thread, but each call must be matched with a corresponding call to <a href="https://msdn.microsoft.com/5ED1A430-27C3-44BA-BF17-B5FB9D4C7087">Deactivate</a> from the same thread.




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

