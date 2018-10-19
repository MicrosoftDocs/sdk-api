---
UID: NF:msctf.ITfContext.InWriteSession
title: ITfContext::InWriteSession
author: windows-sdk-content
description: ITfContext::InWriteSession method
old-location: tsf\itfcontext_inwritesession.htm
tech.root: TSF
ms.assetid: 88a8a2c1-bd5f-47d2-8612-c7e0cabfe254
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfContext interface [Text Services Framework],InWriteSession method, ITfContext.InWriteSession, ITfContext::InWriteSession, InWriteSession, InWriteSession method [Text Services Framework], InWriteSession method [Text Services Framework],ITfContext interface, _tsf_itfcontext_inwritesession_ref, msctf/ITfContext::InWriteSession, tsf.itfcontext_inwritesession
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
 - ITfContext.InWriteSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContext::InWriteSession


## -description




## -parameters




### -param tid [in]

Contains a <b>TfClientID</b> value that identifies the client.


### -param pfWriteSession [out]

Pointer to a <b>BOOL</b> that receives a nonzero value if the client has a read/write lock on the context. Receives zero if the client does not have an edit session or has a read-only edit session.


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
<i>pfWriteSession</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



A client uses this method, from inside a notification callback, to determine if it must make the change.



