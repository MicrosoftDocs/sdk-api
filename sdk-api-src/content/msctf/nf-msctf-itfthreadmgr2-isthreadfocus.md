---
UID: NF:msctf.ITfThreadMgr2.IsThreadFocus
title: ITfThreadMgr2::IsThreadFocus
author: windows-sdk-content
description: Determines if the calling thread has the TSF input focus.
old-location: tsf\itfthreadmgr2_isthreadfocus.htm
tech.root: TSF
ms.assetid: 8440BEE8-865F-4403-8558-C77638290A7F
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfThreadMgr2 interface [Text Services Framework],IsThreadFocus method, ITfThreadMgr2.IsThreadFocus, ITfThreadMgr2::IsThreadFocus, IsThreadFocus, IsThreadFocus method [Text Services Framework], IsThreadFocus method [Text Services Framework],ITfThreadMgr2 interface, msctf/ITfThreadMgr2::IsThreadFocus, tsf.itfthreadmgr2_isthreadfocus
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
 - ITfThreadMgr2.IsThreadFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfThreadMgr2::IsThreadFocus


## -description


Determines if the calling thread has the TSF input focus.


## -parameters




### -param pfThreadFocus [out]

Pointer to a BOOL that receives a value that indicates if the calling thread has input focus. This parameter receives a nonzero value if the calling thread has the focus or zero otherwise.


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
<i>pfThreadFocus</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

