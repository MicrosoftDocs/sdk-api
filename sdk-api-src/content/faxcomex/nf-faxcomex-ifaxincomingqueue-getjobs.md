---
UID: NF:faxcomex.IFaxIncomingQueue.GetJobs
title: IFaxIncomingQueue::GetJobs (faxcomex.h)
author: windows-sdk-content
description: The GetJobs method returns the collection of inbound fax jobs in the queue.
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6p6b.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxIncomingQueue interface, IFaxIncomingQueue interface [Fax Service],GetJobs method, IFaxIncomingQueue.GetJobs, IFaxIncomingQueue::GetJobs, _mfax_faxincomingqueue.getjobs, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp, fax._mfax_faxincomingqueue_getjobs, faxcomex/IFaxIncomingQueue::GetJobs
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
 - IFaxIncomingQueue.GetJobs
 - IFaxIncomingQueue.GetJobs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingQueue::GetJobs


## -description


The <b>GetJobs</b> method returns the collection of inbound fax jobs in the queue.


## -parameters




### -param pFaxIncomingJobs [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms684964(v=VS.85).aspx">IFaxIncomingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms684959(v=VS.85).aspx">FaxIncomingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> and <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686165(v=VS.85).aspx">IFaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692952(v=VS.85).aspx">Visual Basic Example</a>
 

 

