---
UID: NF:tuner.ITuningSpace.get_CLSID
title: ITuningSpace::get_CLSID (tuner.h)
description: The get_CLSID method gets the CLSID of the tuning space as a BSTR.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_CLSID method","ITuningSpace.get_CLSID","ITuningSpace::get_CLSID","ITuningSpaceget_CLSID","get_CLSID","get_CLSID method [Microsoft TV Technologies]","get_CLSID method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_clsid","tuner/ITuningSpace::get_CLSID"]
old-location: mstv\ituningspace_get_clsid.htm
tech.root: mstv
ms.assetid: def4aac2-3d0b-4ce6-9f6b-d13e7c3cc86d
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_CLSID method, ITuningSpace.get_CLSID, ITuningSpace::get_CLSID, ITuningSpaceget_CLSID, get_CLSID, get_CLSID method [Microsoft TV Technologies], get_CLSID method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_clsid, tuner/ITuningSpace::get_CLSID
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - ITuningSpace::get_CLSID
 - tuner/ITuningSpace::get_CLSID
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
 - ITuningSpace.get_CLSID
---

# ITuningSpace::get_CLSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CLSID</b> method gets the CLSID of the tuning space as a <b>BSTR</b>.

## -parameters

### -param SpaceCLSID [out]

Pointer to a variable that receives a string representation of the tuning space CLSID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method provides script access to the <b>IPersist::GetClassID</b> method.

The returned CLSID represents the COM object that implements this tuning space. The CLSID is not guaranteed to be unique to this tuning space, however, because the same object may implement several tuning spaces.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>