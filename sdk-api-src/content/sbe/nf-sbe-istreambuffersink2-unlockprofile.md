---
UID: NF:sbe.IStreamBufferSink2.UnlockProfile
title: IStreamBufferSink2::UnlockProfile
author: windows-sdk-content
description: The UnlockProfile method unlocks the Stream Buffer Sink filter's profile. After the profile is unlocked, you can change the name of the stub file.
old-location: mstv\istreambuffersink2_unlockprofile.htm
old-project: mstv
ms.assetid: 71214ca2-2613-4dbe-a72b-37d4f768ab6b
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IStreamBufferSink2 interface [Microsoft TV Technologies],UnlockProfile method, IStreamBufferSink2.UnlockProfile, IStreamBufferSink2::UnlockProfile, IStreamBufferSink2UnlockProfile, UnlockProfile, UnlockProfile method [Microsoft TV Technologies], UnlockProfile method [Microsoft TV Technologies],IStreamBufferSink2 interface, mstv.istreambuffersink2_unlockprofile, sbe/IStreamBufferSink2::UnlockProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - IStreamBufferSink2.UnlockProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IStreamBufferSink2::UnlockProfile


## -description



      The <b>UnlockProfile</b> method unlocks the Stream Buffer Sink filter's profile. After the profile is unlocked, you can change the name of the stub file.


## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The profile is not currently locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The filter graph must be stopped when you call this method. If the recording session has not been started, this method invalidates the recording. To re-create the recording, call <a href="https://msdn.microsoft.com/9e694cc2-090e-43b1-88c7-77175a930bf1">IStreamBufferSink::LockProfile</a> again. If the profile is not already locked, the <b>UnlockProfile</b> method has no effect and returns S_FALSE.

If the graph is running, stopping the graph automatically unlocks the profile without the need to call <b>UnlockProfile</b>.




## -see-also




<a href="https://msdn.microsoft.com/ae97e1e2-011d-4bb1-ae11-eda401e1d337">IStreamBufferSink2 Interface</a>
 

 

