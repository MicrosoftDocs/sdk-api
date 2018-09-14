---
UID: NF:faxcomex.IFaxAccountIncomingQueue.GetJob
title: IFaxAccountIncomingQueue::GetJob
author: windows-sdk-content
description: Returns an incoming fax job in the job queue of the current fax account according to the job's ID.
old-location: fax\_mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\getjob.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxAccountIncomingQueue interface, IFaxAccountIncomingQueue interface [Fax Service],GetJob method, IFaxAccountIncomingQueue.GetJob, IFaxAccountIncomingQueue::GetJob, _mfax_faxaccountincomingqueue.getjob, fax._mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjob_cpp, fax._mfax_faxaccountincomingqueue_getjob, faxcomex/IFaxAccountIncomingQueue::GetJob
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
 - IFaxAccountIncomingQueue.GetJob
 - IFaxAccountIncomingQueue.GetJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountIncomingQueue::GetJob


## -description


Returns an incoming fax job in the job queue of the current fax account according to the job's ID.


## -parameters




### -param bstrJobId [in]

Type: <b>BSTR</b>

Specifies the job ID.


### -param pFaxIncomingJob [out, retval]

Type: <b><a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>**</b>

A <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_LOW</a> access rights.

If the setting "All incoming faxes are viewable by everyone" is true (see <a href="https://msdn.microsoft.com/f40268ab-6df0-4c4f-9c73-c3129be589cc">IncomingFaxesArePublic</a>) or if the current user has <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the set returned includes all the messages present in the fax server incoming queue.  




## -see-also




<a href="https://msdn.microsoft.com/dd0ba850-d2d0-4ba3-a36c-a0947ab44c28">FaxAccountIncomingQueue</a>



<a href="https://msdn.microsoft.com/4c21ddda-2525-4279-ade9-c8e389b79e76">IFaxAccountIncomingQueue</a>
 

 

