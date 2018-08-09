---
UID: NF:bits.IBackgroundCopyJob.GetDescription
title: IBackgroundCopyJob::GetDescription
author: windows-sdk-content
description: Retrieves the description of the job.
old-location: bits\ibackgroundcopyjob_getdescription.htm
old-project: bits
ms.assetid: 1a791390-2bd8-4732-98a2-74f740cfd822
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDescription, GetDescription method [BITS], GetDescription method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetDescription method, IBackgroundCopyJob.GetDescription, IBackgroundCopyJob::GetDescription, _drz_ibackgroundcopyjob_getdescription, bits.ibackgroundcopyjob_getdescription, bits/IBackgroundCopyJob::GetDescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetDescription
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetDescription


## -description


Retrieves the description of the job.


## -parameters




### -param pVal






#### - ppDescription [out]

Null-terminated string that contains a short description of the job. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppDescription</i> when done.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Description of the job was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter, <i>ppDescription</i>, cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9148ec9b-7a03-4bb3-9644-e52f6cd13073">IBackgroundCopyJob::SetDescription</a>
 

 

