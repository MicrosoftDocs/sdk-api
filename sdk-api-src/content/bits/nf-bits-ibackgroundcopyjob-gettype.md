---
UID: NF:bits.IBackgroundCopyJob.GetType
title: IBackgroundCopyJob::GetType
author: windows-sdk-content
description: Retrieves the type of transfer being performed, such as a file download or upload.
old-location: bits\ibackgroundcopyjob_gettype.htm
tech.root: Bits
ms.assetid: b84c45c2-379a-40d0-91ab-0124f0ef6b00
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetType, GetType method [BITS], GetType method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetType method, IBackgroundCopyJob.GetType, IBackgroundCopyJob::GetType, _drz_ibackgroundcopyjob_gettype, bits.ibackgroundcopyjob_gettype, bits/IBackgroundCopyJob::GetType
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetType


## -description


Retrieves the type of transfer being performed, such as a file download or upload.


## -parameters




### -param pVal

TBD




#### - pJobType [out]

Type of transfer being performed. For a list of transfer types, see the 
<a href="https://msdn.microsoft.com/b341a63f-3a1d-4518-8f05-17d28af603b4">BG_JOB_TYPE</a> enumeration.


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
Transfer type was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pJobType</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Specify the type of transfer when you 
<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">create the job</a>.




## -see-also




<a href="https://msdn.microsoft.com/b341a63f-3a1d-4518-8f05-17d28af603b4">BG_JOB_TYPE</a>



<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a>
 

 

