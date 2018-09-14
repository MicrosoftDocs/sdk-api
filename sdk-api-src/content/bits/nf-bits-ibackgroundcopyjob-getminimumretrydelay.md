---
UID: NF:bits.IBackgroundCopyJob.GetMinimumRetryDelay
title: IBackgroundCopyJob::GetMinimumRetryDelay
author: windows-sdk-content
description: Retrieves the minimum length of time that the service waits after encountering a transient error condition before trying to transfer the file.
old-location: bits\ibackgroundcopyjob_getminimumretrydelay.htm
tech.root: Bits
ms.assetid: af599174-44f8-4d5e-b9ff-61ddbb330580
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetMinimumRetryDelay, GetMinimumRetryDelay method [BITS], GetMinimumRetryDelay method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetMinimumRetryDelay method, IBackgroundCopyJob.GetMinimumRetryDelay, IBackgroundCopyJob::GetMinimumRetryDelay, _drz_ibackgroundcopyjob_getminimumretrydelay, bits.ibackgroundcopyjob_getminimumretrydelay, bits/IBackgroundCopyJob::GetMinimumRetryDelay
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
 - IBackgroundCopyJob.GetMinimumRetryDelay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetMinimumRetryDelay


## -description


Retrieves the minimum length of time that the service waits after encountering a transient error condition before trying to transfer the file.


## -parameters




### -param Seconds

TBD




#### - pRetryDelay [in]

Length of time, in seconds, that the service waits after encountering a transient error before trying to transfer the file.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/4881e5f7-a835-40d5-a056-d6b23e3cd84c">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="https://msdn.microsoft.com/52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6">IBackgroundCopyJob::SetMinimumRetryDelay</a>
 

 

