---
UID: NF:faxcomex.IFaxAccountIncomingQueue.GetJobs
title: IFaxAccountIncomingQueue::GetJobs
author: windows-sdk-content
description: Returns the collection of inbound fax jobs in the queue for the current fax account.
old-location: fax\_mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\getjobs.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxAccountIncomingQueue interface, IFaxAccountIncomingQueue interface [Fax Service],GetJobs method, IFaxAccountIncomingQueue.GetJobs, IFaxAccountIncomingQueue::GetJobs, _mfax_faxaccountincomingqueue.getjobs, fax._mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjobs_cpp, fax._mfax_faxaccountincomingqueue_getjobs, faxcomex/IFaxAccountIncomingQueue::GetJobs
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
---

# IFaxAccountIncomingQueue::GetJobs


## -description


Returns the collection of inbound fax jobs in the queue for the current fax account.


## -parameters




### -param pFaxIncomingJobs [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms684964(v=VS.85).aspx">IFaxIncomingJobs</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms684959(v=VS.85).aspx">FaxIncomingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2SUBMIT_LOW</a> access rights.

If the setting "All incoming faxes are viewable by everyone" is true (see <a href="https://msdn.microsoft.com/en-us/library/Aa358923(v=VS.85).aspx">IncomingFaxesArePublic</a>) or if the current user has <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the set returned includes all the messages present in the fax server incoming queue.  




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358954(v=VS.85).aspx">FaxAccountIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359043(v=VS.85).aspx">IFaxAccountIncomingQueue</a>
 

 

