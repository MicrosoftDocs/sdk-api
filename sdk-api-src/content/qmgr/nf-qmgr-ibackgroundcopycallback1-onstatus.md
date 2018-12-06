---
UID: NF:qmgr.IBackgroundCopyCallback1.OnStatus
title: IBackgroundCopyCallback1::OnStatus
author: windows-sdk-content
description: Implement the OnStatus method to receive notification when the group is complete or an error occurs.
old-location: bits\ibackgroundcopycallback1_onstatus.htm
tech.root: bits
ms.assetid: 88f75a65-8d27-4413-8b00-4caf11fbcc5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyCallback1 interface [BITS],OnStatus method, IBackgroundCopyCallback1.OnStatus, IBackgroundCopyCallback1::OnStatus, OnStatus, OnStatus method [BITS], OnStatus method [BITS],IBackgroundCopyCallback1 interface, bits.ibackgroundcopycallback1_onstatus, qmgr/IBackgroundCopyCallback1::OnStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
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
 - Qmgr.h
api_name:
 - IBackgroundCopyCallback1.OnStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyCallback1::OnStatus


## -description


<p class="CCE_Message">[<b>IBackgroundCopyCallback1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Implement the <b>OnStatus</b> method to receive notification when the group is complete or an error occurs.


## -parameters




### -param pGroup [in]

Interface pointer to the group that generated the event. 


### -param pJob [in]

Interface pointer to the job associated with the event or <b>NULL</b> if the event is not associated with a job.


### -param dwFileIndex [in]

Index to the file associated with the error or -1. To retrieve the file, call the <a href="https://msdn.microsoft.com/6cd680cc-abe0-44e1-a650-079295a8dd4a">IBackgroundCopyJob1::GetFile</a> method. 


### -param dwStatus [in]

The state of the group. The state of the group is either complete (all jobs in the group have been downloaded) or in error. An error occurred if the QM_STATUS_GROUP_ERROR flag is set. Otherwise, the group is complete.


### -param dwNumOfRetries [in]

Number of times QMGR tried to download the group after an error occurs. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set. 


### -param dwWin32Result [in]

Win32 error code. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set.


### -param dwTransportResult [in]

HTTP error code. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set.


## -returns



This method should return <b>S_OK</b>; otherwise, the service continues to call this method until S_OK is returned. The interval at which the implementation is called is arbitrary.




## -see-also




<a href="https://msdn.microsoft.com/d5d22cf6-d9b5-4001-a0ac-f67d59dde779">IBackgroundCopyCallback1</a>
 

 

