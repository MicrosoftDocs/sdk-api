---
UID: NF:tuner.IBDACreateTuneRequestEx.CreateTuneRequestEx
title: IBDACreateTuneRequestEx::CreateTuneRequestEx (tuner.h)
description: Creates a new tuning request for a tuning space. This method enables the caller to specify a particular type of tuning request.
helpviewer_keywords: ["CreateTuneRequestEx","CreateTuneRequestEx method [Microsoft TV Technologies]","CreateTuneRequestEx method [Microsoft TV Technologies]","IBDACreateTuneRequestEx interface","IBDACreateTuneRequestEx interface [Microsoft TV Technologies]","CreateTuneRequestEx method","IBDACreateTuneRequestEx.CreateTuneRequestEx","IBDACreateTuneRequestEx::CreateTuneRequestEx","mstv.ibdacreatetunerequestex_createtunerequestex","tuner/IBDACreateTuneRequestEx::CreateTuneRequestEx"]
old-location: mstv\ibdacreatetunerequestex_createtunerequestex.htm
tech.root: mstv
ms.assetid: bf378da2-be79-484e-84c6-bf1669b50218
ms.date: 12/05/2018
ms.keywords: CreateTuneRequestEx, CreateTuneRequestEx method [Microsoft TV Technologies], CreateTuneRequestEx method [Microsoft TV Technologies],IBDACreateTuneRequestEx interface, IBDACreateTuneRequestEx interface [Microsoft TV Technologies],CreateTuneRequestEx method, IBDACreateTuneRequestEx.CreateTuneRequestEx, IBDACreateTuneRequestEx::CreateTuneRequestEx, mstv.ibdacreatetunerequestex_createtunerequestex, tuner/IBDACreateTuneRequestEx::CreateTuneRequestEx
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDACreateTuneRequestEx::CreateTuneRequestEx
 - tuner/IBDACreateTuneRequestEx::CreateTuneRequestEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IBDACreateTuneRequestEx.CreateTuneRequestEx
---

# IBDACreateTuneRequestEx::CreateTuneRequestEx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Creates a new tuning  request for a tuning space. This method enables the caller to specify a particular type of tuning request.

## -parameters

### -param TuneRequestIID [in]

GUID that identifies the type of <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> object expected by the caller. If this value is <b>NULL</b>, this method behaves the same as <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-createtunerequest">ITuningSpace::CreateTuneRequest</a> and creates an empty (uninitialized) <b>ITuneRequest</b> object.

### -param TuneRequest [out]

Address of a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface of the new tuning request object. The caller must release the interface. If the <i>TuneRequestIID</i> argument is <b>NULL</b>, this address is set to <b>NULL</b> also.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacreatetunerequestex">IBDACreateTuneRequestEx</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-createtunerequest">ITuningSpace::CreateTuneRequest</a>