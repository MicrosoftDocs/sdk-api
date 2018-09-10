---
UID: NF:bits.IBackgroundCopyJob.GetErrorCount
title: IBackgroundCopyJob::GetErrorCount
author: windows-sdk-content
description: Retrieves the number of times BITS tried to transfer the job and an error occurred.
old-location: bits\ibackgroundcopyjob_geterrorcount.htm
tech.root: bits
ms.assetid: 04ca4752-8c4d-4f54-9dfa-3c9f567d7980
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetErrorCount, GetErrorCount method [BITS], GetErrorCount method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetErrorCount method, IBackgroundCopyJob.GetErrorCount, IBackgroundCopyJob::GetErrorCount, _drz_ibackgroundcopyjob_geterrorcount, bits.ibackgroundcopyjob_geterrorcount, bits/IBackgroundCopyJob::GetErrorCount
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
 - IBackgroundCopyJob.GetErrorCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetErrorCount


## -description


Retrieves the number of times BITS tried to transfer the job and an error occurred.


## -parameters




### -param Errors

TBD




#### - pErrors [out]

Number of errors that occurred while BITS tried to transfer the job. The count increases  when the job moves from the BG_JOB_STATE_TRANSFERRING state to the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state. 


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The count is never reset. The count may not accurately reflect the number of times the job moves to the transient error or error state. For example, BITS does not increase the count when network disconnects occur, the check disk program runs, or the bandwidth policy prevents jobs from transferring. 

BITS also increases the count each time it tries to transfer the job when the job is in the transient error state and the job fails.

<b>BITS 1.5 and earlier:  </b> BITS does not increase the count each time it tries to transfer the job when it is in the transient error state.




## -see-also




<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a>
 

 

