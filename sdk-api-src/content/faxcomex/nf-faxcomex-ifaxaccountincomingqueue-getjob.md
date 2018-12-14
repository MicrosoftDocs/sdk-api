---
UID: NF:faxcomex.IFaxAccountIncomingQueue.GetJob
title: IFaxAccountIncomingQueue::GetJob
author: windows-sdk-content
description: Returns an incoming fax job in the job queue of the current fax account according to the job's ID.
old-location: fax\_mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\getjob.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms684878(v=VS.85).aspx">IFaxIncomingJob</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2SUBMIT_LOW</a> access rights.

If the setting "All incoming faxes are viewable by everyone" is true (see <a href="https://msdn.microsoft.com/en-us/library/Aa358923(v=VS.85).aspx">IncomingFaxesArePublic</a>) or if the current user has <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the set returned includes all the messages present in the fax server incoming queue.  




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358954(v=VS.85).aspx">FaxAccountIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359043(v=VS.85).aspx">IFaxAccountIncomingQueue</a>
 

 

