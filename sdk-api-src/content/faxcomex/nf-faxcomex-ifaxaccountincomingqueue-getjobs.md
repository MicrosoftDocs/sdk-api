---
UID: NF:faxcomex.IFaxAccountIncomingQueue.GetJobs
title: IFaxAccountIncomingQueue::GetJobs
author: windows-sdk-content
description: Returns the collection of inbound fax jobs in the queue for the current fax account.
old-location: fax\_mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\getjobs.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxAccountIncomingQueue interface, IFaxAccountIncomingQueue interface [Fax Service],GetJobs method, IFaxAccountIncomingQueue.GetJobs, IFaxAccountIncomingQueue::GetJobs, _mfax_faxaccountincomingqueue.getjobs, fax._mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjobs_cpp, fax._mfax_faxaccountincomingqueue_getjobs, faxcomex/IFaxAccountIncomingQueue::GetJobs
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
 - IFaxAccountIncomingQueue.GetJobs
 - IFaxAccountIncomingQueue.GetJobs
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
- IFaxAccountIncomingQueue.GetJobs
: 
---

# IFaxAccountIncomingQueue::GetJobs


## -description


Returns the collection of inbound fax jobs in the queue for the current fax account.


## -parameters




### -param pFaxIncomingJobs [out, retval]

Type: <b><a href="https://msdn.microsoft.com/970a6047-4c85-404d-ad7e-39703f09f856">IFaxIncomingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_LOW</a> access rights.

If the setting "All incoming faxes are viewable by everyone" is true (see <a href="https://msdn.microsoft.com/f40268ab-6df0-4c4f-9c73-c3129be589cc">IncomingFaxesArePublic</a>) or if the current user has <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the set returned includes all the messages present in the fax server incoming queue.  




## -see-also




<a href="https://msdn.microsoft.com/dd0ba850-d2d0-4ba3-a36c-a0947ab44c28">FaxAccountIncomingQueue</a>



<a href="https://msdn.microsoft.com/4c21ddda-2525-4279-ade9-c8e389b79e76">IFaxAccountIncomingQueue</a>
 

 

