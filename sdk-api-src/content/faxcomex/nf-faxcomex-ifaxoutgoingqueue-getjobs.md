---
UID: NF:faxcomex.IFaxOutgoingQueue.GetJobs
title: IFaxOutgoingQueue::GetJobs
author: windows-sdk-content
description: The IFaxOutgoingQueue::GetJobs method returns a collection of the outbound fax jobs in the job queue.
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_978z.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],GetJobs method, IFaxOutgoingQueue.GetJobs, IFaxOutgoingQueue::GetJobs, _mfax_faxoutgoingqueue.getjobs, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_getjobs_cpp, fax._mfax_faxoutgoingqueue_getjobs, faxcomex/IFaxOutgoingQueue::GetJobs
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFaxOutgoingQueue.GetJobs
 - IFaxOutgoingQueue.GetJobs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingQueue::GetJobs


## -description


The <b>IFaxOutgoingQueue::GetJobs</b> method returns a collection of the outbound fax jobs in the job queue.


## -parameters




### -param pFaxOutgoingJobs [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> access right.

With the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access right, users can use this method only for their own faxes. With the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> access right, users can use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687528(v=VS.85).aspx">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687529(v=VS.85).aspx">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693393(v=VS.85).aspx">Managing Outgoing Jobs</a>
 

 

