---
UID: NF:faxcomex._IFaxAccountNotify.OnIncomingJobRemoved
title: _IFaxAccountNotify::OnIncomingJobRemoved (faxcomex.h)
description: Called by the fax service when an incoming fax job is removed from the job queue of a particular fax account.
helpviewer_keywords: ["IFaxAccountNotify.OnIncomingJobRemoved","OnIncomingJobRemoved","OnIncomingJobRemoved method [Fax Service]","OnIncomingJobRemoved method [Fax Service]","_IFaxAccountNotify interface","_IFaxAccountNotify interface [Fax Service]","OnIncomingJobRemoved method","_IFaxAccountNotify.OnIncomingJobRemoved","_IFaxAccountNotify::OnIncomingJobRemoved","_mfax_ifaxaccountnotify_onincomingjobremoved","fax._mfax_ifaxaccountnotify_onincomingjobremoved","faxcomex/_IFaxAccountNotify::OnIncomingJobRemoved"]
old-location: fax\_mfax_ifaxaccountnotify_onincomingjobremoved.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\onincomingjobremoved.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountNotify.OnIncomingJobRemoved, OnIncomingJobRemoved, OnIncomingJobRemoved method [Fax Service], OnIncomingJobRemoved method [Fax Service],_IFaxAccountNotify interface, _IFaxAccountNotify interface [Fax Service],OnIncomingJobRemoved method, _IFaxAccountNotify.OnIncomingJobRemoved, _IFaxAccountNotify::OnIncomingJobRemoved, _mfax_ifaxaccountnotify_onincomingjobremoved, fax._mfax_ifaxaccountnotify_onincomingjobremoved, faxcomex/_IFaxAccountNotify::OnIncomingJobRemoved
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IFaxAccountNotify::OnIncomingJobRemoved
 - faxcomex/_IFaxAccountNotify::OnIncomingJobRemoved
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - _IFaxAccountNotify.OnIncomingJobRemoved
 - IFaxAccountNotify.OnIncomingJobRemoved
---

# _IFaxAccountNotify::OnIncomingJobRemoved


## -description

Called by the fax service when an incoming fax job is removed from the job queue of a particular fax account.

## -parameters

### -param pFaxAccount [in]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>*</b>

An <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.

### -param bstrJobId [in]

Type: <b>BSTR</b>

A null-terminated string that contains the ID of the job removed from the job queue.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To implement this functionality in Visual Basic, select and implement the appropriate event procedure.

## -see-also

<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxaccountnotify">IFaxAccountNotify</a>