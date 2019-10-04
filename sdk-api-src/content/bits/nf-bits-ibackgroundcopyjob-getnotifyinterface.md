---
UID: NF:bits.IBackgroundCopyJob.GetNotifyInterface
title: IBackgroundCopyJob::GetNotifyInterface (bits.h)
author: windows-sdk-content
description: Retrieves the interface pointer to your implementation of the IBackgroundCopyCallback interface.
old-location: bits\ibackgroundcopyjob_getnotifyinterface.htm
tech.root: Bits
ms.assetid: 6a954fbc-baf6-4efa-bec0-dd86b4b7a916
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNotifyInterface, GetNotifyInterface method [BITS], GetNotifyInterface method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetNotifyInterface method, IBackgroundCopyJob.GetNotifyInterface, IBackgroundCopyJob::GetNotifyInterface, _drz_ibackgroundcopyjob_getnotifyinterface, bits.ibackgroundcopyjob_getnotifyinterface, bits/IBackgroundCopyJob::GetNotifyInterface
ms.topic: method
f1_keywords: 
 - "bits/IBackgroundCopyJob.GetNotifyInterface"
dev_langs:
 - c++
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
 - IBackgroundCopyJob.GetNotifyInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyJob::GetNotifyInterface


## -description


Retrieves the interface pointer to your implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface.


## -parameters




### -param pVal [out]

Interface pointer to your implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface. When done, release <i>ppNotifyInterface</i>.


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
Notification interface pointer was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Must pass the address of the <i>ppNotifyInterface</i> interface pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnotifyflags">IBackgroundCopyJob::GetNotifyFlags</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a>
 

 

