---
UID: NF:faxcomex.IFaxAccountOutgoingQueue.GetJobs
title: IFaxAccountOutgoingQueue::GetJobs
author: windows-sdk-content
description: Returns the collection of outbound fax jobs in the queue for the current fax account.
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\getjobs.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxAccountOutgoingQueue interface, IFaxAccountOutgoingQueue interface [Fax Service],GetJobs method, IFaxAccountOutgoingQueue.GetJobs, IFaxAccountOutgoingQueue::GetJobs, _mfax_faxaccountoutgoingqueue.getjobs, fax._mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp, fax._mfax_faxaccountoutgoingqueue_getjobs, faxcomex/IFaxAccountOutgoingQueue::GetJobs
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccountOutgoingQueue.GetJobs
 - IFaxAccountOutgoingQueue.GetJobs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountOutgoingQueue::GetJobs


## -description


Returns the collection of outbound fax jobs in the queue for the current fax account.


## -parameters




### -param pFaxOutgoingJobs [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms689507(v=VS.85).aspx">IFaxOutgoingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358945(v=VS.85).aspx">FaxAccountOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359022(v=VS.85).aspx">IFaxAccountOutgoingQueue</a>
 

 

