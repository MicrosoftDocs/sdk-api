---
UID: NF:faxcomex.IFaxAccountIncomingQueue.GetJobs
title: IFaxAccountIncomingQueue::GetJobs (faxcomex.h)
author: windows-sdk-content
description: Returns the collection of inbound fax jobs in the queue for the current fax account.
old-location: fax\_mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\getjobs.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxAccountIncomingQueue interface, IFaxAccountIncomingQueue interface [Fax Service],GetJobs method, IFaxAccountIncomingQueue.GetJobs, IFaxAccountIncomingQueue::GetJobs, _mfax_faxaccountincomingqueue.getjobs, fax._mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjobs_cpp, fax._mfax_faxaccountincomingqueue_getjobs, faxcomex/IFaxAccountIncomingQueue::GetJobs
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxAccountIncomingQueue.GetJobs"
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
ms.custom: 19H1
---

# IFaxAccountIncomingQueue::GetJobs


## -description


Returns the collection of inbound fax jobs in the queue for the current fax account.


## -parameters




### -param pFaxIncomingJobs [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a>**</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_LOW</a> access rights.

If the setting "All incoming faxes are viewable by everyone" is true (see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-incomingfaxesarepublic-vb">IncomingFaxesArePublic</a>) or if the current user has <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the set returned includes all the messages present in the fax server incoming queue.  




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingqueue">FaxAccountIncomingQueue</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingqueue">IFaxAccountIncomingQueue</a>
 

 

