---
UID: NF:faxcomex.IFaxIncomingQueue.GetJob
title: IFaxIncomingQueue::GetJob (faxcomex.h)
author: windows-sdk-content
description: The GetJob method returns an incoming fax job in the job queue according to its ID.
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6crm.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxIncomingQueue interface, IFaxIncomingQueue interface [Fax Service],GetJob method, IFaxIncomingQueue.GetJob, IFaxIncomingQueue::GetJob, _mfax_faxincomingqueue.getjob, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjob_cpp, fax._mfax_faxincomingqueue_getjob, faxcomex/IFaxIncomingQueue::GetJob
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingQueue.GetJob
 - IFaxIncomingQueue.GetJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingQueue::GetJob


## -description


The <b>GetJob</b> method returns an incoming fax job in the job queue according to its ID.


## -parameters




### -param bstrJobId [in]

Type: <b>BSTR</b>

Specifies the job ID.


### -param pFaxIncomingJob [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms684878(v=VS.85).aspx">IFaxIncomingJob</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> and <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686165(v=VS.85).aspx">IFaxIncomingQueue</a>
 

 

