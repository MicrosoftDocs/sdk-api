---
UID: NF:faxcomex.IFaxOutgoingQueue.GetJob
title: IFaxOutgoingQueue::GetJob
author: windows-sdk-content
description: The GetJob method returns an outbound fax job in the job queue according to its ID.
old-location: fax\_mfax_faxoutgoingqueue_getjob.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3w6a.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FaxOutgoingQueue object [Fax Service],GetJob method, FaxOutgoingQueue.GetJob, GetJob, GetJob method [Fax Service], GetJob method [Fax Service],FaxOutgoingQueue object, IFaxOutgoingQueue.GetJob, IFaxOutgoingQueue::GetJob, _mfax_faxoutgoingqueue.getjob, fax._mfax_faxoutgoingqueue_getjob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingQueue.GetJob
 - IFaxOutgoingQueue.GetJob
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingQueue::GetJob


## -description


The <b>GetJob</b> method returns an outbound fax job in the job queue according to its ID.


## -parameters




### -param bstrJobId [in]

Type: <b>String</b>

Specifies the job ID. 


### -param pFaxOutgoingJob






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a>**</b>

A <a href="https://msdn.microsoft.com/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a> object.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> access right.

With the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access right, users can use this method only for their own faxes. With the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> access right, users can use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/library/ms687528(v=VS.85).aspx">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/library/ms687529(v=VS.85).aspx">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/library/ms693393(v=VS.85).aspx">Managing Outgoing Jobs</a>
 

 

