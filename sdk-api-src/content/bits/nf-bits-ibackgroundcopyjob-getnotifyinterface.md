---
UID: NF:bits.IBackgroundCopyJob.GetNotifyInterface
title: IBackgroundCopyJob::GetNotifyInterface method
author: windows-driver-content
description: Retrieves the interface pointer to your implementation of the IBackgroundCopyCallback interface.
old-location: bits\ibackgroundcopyjob_getnotifyinterface.htm
old-project: Bits
ms.assetid: 6a954fbc-baf6-4efa-bec0-dd86b4b7a916
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetNotifyInterface method [BITS], GetNotifyInterface method [BITS], IBackgroundCopyJob interface, GetNotifyInterface,IBackgroundCopyJob.GetNotifyInterface, IBackgroundCopyJob, IBackgroundCopyJob interface [BITS], GetNotifyInterface method, IBackgroundCopyJob::GetNotifyInterface, _drz_ibackgroundcopyjob_getnotifyinterface, bits.ibackgroundcopyjob_getnotifyinterface, bits/IBackgroundCopyJob::GetNotifyInterface
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyJob.GetNotifyInterface
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetNotifyInterface method


## -description


Retrieves the interface pointer to your implementation of the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface.


## -parameters




### -param pVal






#### - ppNotifyInterface [out]

Interface pointer to your implementation of the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface. When done, release <i>ppNotifyInterface</i>.


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




<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/a4407816-a4c5-4734-9686-46d5a8133c2f">IBackgroundCopyJob::GetNotifyFlags</a>



<a href="https://msdn.microsoft.com/34d51546-ec27-471f-9da5-3bec7ed4e1ea">IBackgroundCopyJob::SetNotifyInterface</a>
 

 

