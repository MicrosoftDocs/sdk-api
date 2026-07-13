---
UID: NF:faxcomex._IFaxAccountNotify.OnIncomingJobChanged
title: _IFaxAccountNotify::OnIncomingJobChanged (faxcomex.h)
description: Called by the fax service when the status of an incoming fax job for a particular fax account changes.
helpviewer_keywords: ["IFaxAccountNotify.OnIncomingJobChanged","OnIncomingJobChanged","OnIncomingJobChanged method [Fax Service]","OnIncomingJobChanged method [Fax Service]","_IFaxAccountNotify interface","_IFaxAccountNotify interface [Fax Service]","OnIncomingJobChanged method","_IFaxAccountNotify.OnIncomingJobChanged","_IFaxAccountNotify::OnIncomingJobChanged","_mfax_ifaxaccountnotify_onincomingjobchanged","fax._mfax_ifaxaccountnotify_onincomingjobchanged","faxcomex/_IFaxAccountNotify::OnIncomingJobChanged"]
old-location: fax\_mfax_ifaxaccountnotify_onincomingjobchanged.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\onincomingjobchanged.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountNotify.OnIncomingJobChanged, OnIncomingJobChanged, OnIncomingJobChanged method [Fax Service], OnIncomingJobChanged method [Fax Service],_IFaxAccountNotify interface, _IFaxAccountNotify interface [Fax Service],OnIncomingJobChanged method, _IFaxAccountNotify.OnIncomingJobChanged, _IFaxAccountNotify::OnIncomingJobChanged, _mfax_ifaxaccountnotify_onincomingjobchanged, fax._mfax_ifaxaccountnotify_onincomingjobchanged, faxcomex/_IFaxAccountNotify::OnIncomingJobChanged
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
 - _IFaxAccountNotify::OnIncomingJobChanged
 - faxcomex/_IFaxAccountNotify::OnIncomingJobChanged
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
 - _IFaxAccountNotify.OnIncomingJobChanged
 - IFaxAccountNotify.OnIncomingJobChanged
---

# _IFaxAccountNotify::OnIncomingJobChanged


## -description

Called by the fax service when the status of an incoming fax job for a particular fax account changes.

## -parameters

### -param pFaxAccount [in]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>*</b>

An <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.

### -param bstrJobId [in]

Type: <b>BSTR</b>

A null-terminated string that contains the ID of the job for which the status has changed.

### -param pJobStatus [in]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxjobstatus">IFaxJobStatus</a>*</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus">FaxJobStatus</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To implement this functionality in Visual Basic, select and implement the appropriate event procedure.

## -see-also

<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxaccountnotify">IFaxAccountNotify</a>