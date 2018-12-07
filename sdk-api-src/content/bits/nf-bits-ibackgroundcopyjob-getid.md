---
UID: NF:bits.IBackgroundCopyJob.GetId
title: IBackgroundCopyJob::GetId
author: windows-sdk-content
description: Retrieves the identifier used to identify the job in the queue.
old-location: bits\ibackgroundcopyjob_getid.htm
tech.root: bits
ms.assetid: bc214b2e-fbf3-446e-abce-56e515dcfadf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetId, GetId method [BITS], GetId method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetId method, IBackgroundCopyJob.GetId, IBackgroundCopyJob::GetId, _drz_ibackgroundcopyjob_getid, bits.ibackgroundcopyjob_getid, bits/IBackgroundCopyJob::GetId
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
 - IBackgroundCopyJob.GetId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::GetId


## -description


Retrieves the identifier used to identify the job in the queue.


## -parameters




### -param pVal [out]

GUID that identifies the job within the BITS queue.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The service generates the identifier when you 
<a href="https://msdn.microsoft.com/en-us/library/Aa363051(v=VS.85).aspx">create</a> the job. To use the identifier to retrieve an 
<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a> interface pointer for the job, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363060(v=VS.85).aspx">IBackgroundCopyManager::GetJob</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363051(v=VS.85).aspx">IBackgroundCopyManager::CreateJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363060(v=VS.85).aspx">IBackgroundCopyManager::GetJob</a>
 

 

