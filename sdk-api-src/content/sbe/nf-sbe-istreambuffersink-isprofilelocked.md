---
UID: NF:sbe.IStreamBufferSink.IsProfileLocked
title: IStreamBufferSink::IsProfileLocked
author: windows-sdk-content
description: This topic applies only to Windows XP Service Pack 1 or later.
old-location: mstv\istreambuffersink_isprofilelocked.htm
old-project: mstv
ms.assetid: 941c1702-2ef2-4afe-933c-78ed9ee8690b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IStreamBufferSink interface [Microsoft TV Technologies],IsProfileLocked method, IStreamBufferSink.IsProfileLocked, IStreamBufferSink::IsProfileLocked, IStreamBufferSinkIsProfileLocked, IsProfileLocked, IsProfileLocked method [Microsoft TV Technologies], IsProfileLocked method [Microsoft TV Technologies],IStreamBufferSink interface, mstv.istreambuffersink_isprofilelocked, sbe/IStreamBufferSink::IsProfileLocked
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferSink.IsProfileLocked
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IStreamBufferSink::IsProfileLocked


## -description



This topic applies only to Windows XP Service Pack 1 or later.
        



The <b>IsProfileLocked</b> method queries whether the Stream Buffer Sink filter's profile is locked.


## -parameters






## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The profile is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The profile is not locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -remarks



When the filter's profile is locked, the number of streams and their media types are fixed. For more information, see <a href="https://msdn.microsoft.com/9e694cc2-090e-43b1-88c7-77175a930bf1">IStreamBufferSink::LockProfile</a>.




## -see-also




<a href="https://msdn.microsoft.com/4ae5a9e9-da51-4034-9a2c-22b57374deac">IStreamBufferSink Interface</a>
 

 

