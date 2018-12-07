---
UID: NF:faxcomex.IFaxIncomingQueue.GetJobs
title: IFaxIncomingQueue::GetJobs
author: windows-sdk-content
description: The GetJobs method returns the collection of inbound fax jobs in the queue.
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6p6b.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxIncomingQueue interface, IFaxIncomingQueue interface [Fax Service],GetJobs method, IFaxIncomingQueue.GetJobs, IFaxIncomingQueue::GetJobs, _mfax_faxincomingqueue.getjobs, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp, fax._mfax_faxincomingqueue_getjobs, faxcomex/IFaxIncomingQueue::GetJobs
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

Type: <b><a href="https://msdn.microsoft.com/970a6047-4c85-404d-ad7e-39703f09f856">IFaxIncomingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_JOBS</a> and <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/291f8709-c10f-4041-864f-82431edd7fab">IFaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/88cde2d4-09ee-4fbf-8a75-35de58dd45f5">Visual Basic Example</a>
 

 

