---
UID: NF:faxcomex._IFaxAccountNotify.OnOutgoingJobAdded
title: _IFaxAccountNotify::OnOutgoingJobAdded (faxcomex.h)
author: windows-sdk-content
description: Called by the fax service when an outgoing fax job is added to the job queue for a particular fax account.
old-location: fax\_mfax_ifaxaccountnotify_onoutgoingjobadded.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\onoutgoingjobadded.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxAccountNotify.OnOutgoingJobAdded, OnOutgoingJobAdded, OnOutgoingJobAdded method [Fax Service], OnOutgoingJobAdded method [Fax Service],_IFaxAccountNotify interface, _IFaxAccountNotify interface [Fax Service],OnOutgoingJobAdded method, _IFaxAccountNotify.OnOutgoingJobAdded, _IFaxAccountNotify::OnOutgoingJobAdded, _mfax_ifaxaccountnotify_onoutgoingjobadded, fax._mfax_ifaxaccountnotify_onoutgoingjobadded, faxcomex/_IFaxAccountNotify::OnOutgoingJobAdded
ms.topic: method
f1_keywords: 
 - "faxcomex/_IFaxAccountNotify.OnOutgoingJobAdded"
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
 - _IFaxAccountNotify.OnOutgoingJobAdded
 - IFaxAccountNotify.OnOutgoingJobAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxAccountNotify::OnOutgoingJobAdded


## -description


Called by the fax service when an outgoing fax job is added to the job queue for a particular fax account.


## -parameters




### -param pFaxAccount [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>*</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.


### -param bstrJobId [in]

Type: <b>BSTR</b>

Null-terminated string that contains the ID of the job added to the job queue.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. 




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nn-faxcomex-_ifaxaccountnotify">IFaxAccountNotify</a>
 

 

