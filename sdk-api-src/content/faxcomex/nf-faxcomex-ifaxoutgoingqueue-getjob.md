---
UID: NF:faxcomex.IFaxOutgoingQueue.GetJob
title: IFaxOutgoingQueue::GetJob
author: windows-sdk-content
description: The IFaxOutgoingQueue::GetJob method returns an outbound fax job in the job queue according to its ID.
old-location: fax\_mfax_faxoutgoingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3w6a_cpp.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],GetJob method, IFaxOutgoingQueue.GetJob, IFaxOutgoingQueue::GetJob, _mfax_faxoutgoingqueue.getjob_cpp, fax._mfax_faxoutgoingqueue_getjob_cpp, faxcomex/IFaxOutgoingQueue::GetJob
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
 - IFaxOutgoingQueue.GetJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxOutgoingQueue.GetJob
: 
---

# IFaxOutgoingQueue::GetJob


## -description


The <b>IFaxOutgoingQueue::GetJob</b> method returns an outbound fax job in the job queue according to its ID.


## -parameters




### -param bstrJobId [in]

Type: <b>BSTR</b>

Specifies the job ID. 


### -param pFaxOutgoingJob [out, retval]

Type: <b><a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a>**</b>

The address of a pointer that receives a <a href="https://msdn.microsoft.com/en-us/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a> object. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> access right.

With the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access right, users can use this method only for their own faxes. With the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_JOBS</a> access right, users can use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687528(v=VS.85).aspx">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687529(v=VS.85).aspx">IFaxOutgoingQueue</a>
 

 

