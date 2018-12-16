---
UID: NF:faxcomex.IFaxAccountOutgoingQueue.GetJob
title: IFaxAccountOutgoingQueue::GetJob
author: windows-sdk-content
description: Returns an outgoing fax job in the job queue of the current fax account according to the job's ID.
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\getjob.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxAccountOutgoingQueue interface, IFaxAccountOutgoingQueue interface [Fax Service],GetJob method, IFaxAccountOutgoingQueue.GetJob, IFaxAccountOutgoingQueue::GetJob, _mfax_faxaccountoutgoingqueue.getjob, fax._mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjob_cpp, fax._mfax_faxaccountoutgoingqueue_getjob, faxcomex/IFaxAccountOutgoingQueue::GetJob
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
 - IFaxAccountOutgoingQueue.GetJob
 - IFaxAccountOutgoingQueue.GetJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountOutgoingQueue::GetJob


## -description


Returns an outgoing fax job in the job queue of the current fax account according to the job's ID.


## -parameters




### -param bstrJobId [in]

Type: <b>BSTR</b>

Specifies the job ID.


### -param pFaxOutgoingJob [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa358991(v=VS.85).aspx">IFaxOutgoingJob2</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358945(v=VS.85).aspx">FaxAccountOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359022(v=VS.85).aspx">IFaxAccountOutgoingQueue</a>
 

 

