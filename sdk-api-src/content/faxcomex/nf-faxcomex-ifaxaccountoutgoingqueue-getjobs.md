---
UID: NF:faxcomex.IFaxAccountOutgoingQueue.GetJobs
title: IFaxAccountOutgoingQueue::GetJobs
author: windows-sdk-content
description: Returns the collection of outbound fax jobs in the queue for the current fax account.
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\getjobs.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxAccountOutgoingQueue interface, IFaxAccountOutgoingQueue interface [Fax Service],GetJobs method, IFaxAccountOutgoingQueue.GetJobs, IFaxAccountOutgoingQueue::GetJobs, _mfax_faxaccountoutgoingqueue.getjobs, fax._mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp, fax._mfax_faxaccountoutgoingqueue_getjobs, faxcomex/IFaxAccountOutgoingQueue::GetJobs
ms.prod: windows-hardware
ms.technology: windows-devices
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

Type: <b><a href="https://msdn.microsoft.com/0d666ce6-b027-4650-8835-eac445b376a9">IFaxOutgoingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/cfd8e842-838e-41d7-97c0-e75be908c5a0">FaxOutgoingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1012b13-e629-4449-9b7c-c182dad56a9b">FaxAccountOutgoingQueue</a>



<a href="https://msdn.microsoft.com/a790a46a-f685-4f3f-a2d8-b291aa15286a">IFaxAccountOutgoingQueue</a>
 

 

