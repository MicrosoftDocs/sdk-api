---
UID: NF:tuner.ITuningSpace.get_NetworkType
title: ITuningSpace::get_NetworkType (tuner.h)
description: The get_NetworkType method retrieves the network type of the tuning space as a BSTR.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_NetworkType method","ITuningSpace.get_NetworkType","ITuningSpace::get_NetworkType","ITuningSpaceget_NetworkType","get_NetworkType","get_NetworkType method [Microsoft TV Technologies]","get_NetworkType method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_networktype","tuner/ITuningSpace::get_NetworkType"]
old-location: mstv\ituningspace_get_networktype.htm
tech.root: mstv
ms.assetid: f264b6b3-98ae-44bc-8922-ab35c3b7a0d1
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_NetworkType method, ITuningSpace.get_NetworkType, ITuningSpace::get_NetworkType, ITuningSpaceget_NetworkType, get_NetworkType, get_NetworkType method [Microsoft TV Technologies], get_NetworkType method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_networktype, tuner/ITuningSpace::get_NetworkType
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
 - ITuningSpace::get_NetworkType
 - tuner/ITuningSpace::get_NetworkType
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
 - ITuningSpace.get_NetworkType
---

# ITuningSpace::get_NetworkType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_NetworkType</b> method retrieves the network type of the tuning space as a <b>BSTR</b>.



This method is intended for Automation clients, because it returns the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get__networktype">ITuningSpace::get__NetworkType</a> method instead, which returns a GUID value

## -parameters

### -param NetworkTypeGuid [out]

Pointer to a variable that receives a string containing the network type GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>