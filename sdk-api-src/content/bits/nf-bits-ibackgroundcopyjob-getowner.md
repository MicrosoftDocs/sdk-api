---
UID: NF:bits.IBackgroundCopyJob.GetOwner
title: IBackgroundCopyJob::GetOwner
author: windows-sdk-content
description: Retrieves the identity of the job's owner.
old-location: bits\ibackgroundcopyjob_getowner.htm
tech.root: Bits
ms.assetid: 20a645d4-57ab-4b9c-b31a-b8dbb98ea550
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOwner, GetOwner method [BITS], GetOwner method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetOwner method, IBackgroundCopyJob.GetOwner, IBackgroundCopyJob::GetOwner, _drz_ibackgroundcopyjob_getowner, bits.ibackgroundcopyjob_getowner, bits/IBackgroundCopyJob::GetOwner
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
 - IBackgroundCopyJob.GetOwner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetOwner


## -description


Retrieves the identity of the job's owner.


## -parameters




### -param pVal [out]

Null-terminated string that contains the string version of the SID that identifies the job's owner. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppOwner</i> when done.


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
Job owner's identity was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppOwner</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To convert the string format of the SID into a domain\user-name format, which is suitable for display in a user interface, call the following functions:

<ul>
<li>To convert the string SID to a SID, call the 
<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a> function.</li>
<li>To retrieve the domain and user name associated with the SID, call the 
<a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a> function.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12ac2dd8-516b-4b5d-a2bf-0abb55d18ee0">IBackgroundCopyJob::TakeOwnership</a>
 

 

