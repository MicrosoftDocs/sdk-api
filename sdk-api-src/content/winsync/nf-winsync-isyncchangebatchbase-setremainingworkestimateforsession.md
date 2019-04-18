---
UID: NF:winsync.ISyncChangeBatchBase.SetRemainingWorkEstimateForSession
title: ISyncChangeBatchBase::SetRemainingWorkEstimateForSession (winsync.h)
author: windows-sdk-content
description: Sets the estimate of the remaining work for the session.
old-location: winsync\isyncchangebatchbase_setremainingworkestimateforsession.htm
tech.root: winsync
ms.assetid: f73d13d9-244e-4ec1-aacd-047331b13a4d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],SetRemainingWorkEstimateForSession method, ISyncChangeBatchBase.SetRemainingWorkEstimateForSession, ISyncChangeBatchBase::SetRemainingWorkEstimateForSession, SetRemainingWorkEstimateForSession, SetRemainingWorkEstimateForSession method [Windows Sync], SetRemainingWorkEstimateForSession method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_setremainingworkestimateforsession, winsync/ISyncChangeBatchBase::SetRemainingWorkEstimateForSession
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - ISyncChangeBatchBase.SetRemainingWorkEstimateForSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchBase::SetRemainingWorkEstimateForSession


## -description


Sets the estimate of the remaining work for the session.


## -parameters




### -param dwRemainingWorkForSession [in]

The estimate of the remaining work for the session.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The work estimate is determined by the provider.

This value is reported in the <a href="https://msdn.microsoft.com/4a4dad07-b169-4767-a118-3b5c6c8b9764">OnProgress</a> event. If this value is set to zero, the <a href="https://msdn.microsoft.com/4a4dad07-b169-4767-a118-3b5c6c8b9764">OnProgress</a> event will fire for each change that is applied during the session. It will pass zero for the completed work and total work.




## -see-also




<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

