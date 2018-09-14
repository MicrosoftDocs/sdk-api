---
UID: NF:sbe.IStreamBufferRecComp.Initialize
title: IStreamBufferRecComp::Initialize
author: windows-sdk-content
description: The Initialize method sets the file name and the profile for the new recording. Call this method once, after creating the RecComp object.
old-location: mstv\istreambufferreccomp_initialize.htm
tech.root: MSTV
ms.assetid: 97a8519f-2377-43e9-b1ba-7d407caa44a9
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IStreamBufferRecComp interface [Microsoft TV Technologies],Initialize method, IStreamBufferRecComp.Initialize, IStreamBufferRecComp::Initialize, IStreamBufferRecCompInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IStreamBufferRecComp interface, mstv.istreambufferreccomp_initialize, sbe/IStreamBufferRecComp::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecComp.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferRecComp::Initialize


## -description



The <b>Initialize</b> method sets the file name and the profile for the new recording. Call this method once, after creating the <a href="https://msdn.microsoft.com/4f7fcdee-f6e2-4288-a11c-f0076858be67">RecComp</a> object.




## -parameters




### -param pszTargetFilename [in]

Null-terminated, wide character string that specifies the file name of the new recording.


### -param pszSBRecProfileRef [in]

Null-terminated, wide character string that specifies an existing file. This file must be a complete recording, already created by the Stream Buffer Engine.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
Success

</td>
</tr>
</table>
 




## -remarks



The profile of the file specified by <i>pszSBRecProfileRef</i> will be used for the target file. All files that are appended to the target file must have the same profile. For more information about profiles, see <a href="https://msdn.microsoft.com/9e694cc2-090e-43b1-88c7-77175a930bf1">IStreamBufferSink::LockProfile</a>.




## -see-also




<a href="https://msdn.microsoft.com/2998d606-d5ee-4dc3-a4da-57c597c6b594">IStreamBufferRecComp Interface</a>
 

 

