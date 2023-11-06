---
UID: NF:tuner.ITuningSpace.get_UniqueName
title: ITuningSpace::get_UniqueName (tuner.h)
description: The get_UniqueName method retrieves the unique name of the tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_UniqueName method","ITuningSpace.get_UniqueName","ITuningSpace::get_UniqueName","ITuningSpaceget_UniqueName","get_UniqueName","get_UniqueName method [Microsoft TV Technologies]","get_UniqueName method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_uniquename","tuner/ITuningSpace::get_UniqueName"]
old-location: mstv\ituningspace_get_uniquename.htm
tech.root: mstv
ms.assetid: 5c605f8c-7b0c-478d-a823-19e2f396953a
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_UniqueName method, ITuningSpace.get_UniqueName, ITuningSpace::get_UniqueName, ITuningSpaceget_UniqueName, get_UniqueName, get_UniqueName method [Microsoft TV Technologies], get_UniqueName method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_uniquename, tuner/ITuningSpace::get_UniqueName
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
 - ITuningSpace::get_UniqueName
 - tuner/ITuningSpace::get_UniqueName
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
 - ITuningSpace.get_UniqueName
---

# ITuningSpace::get_UniqueName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_UniqueName</b> method retrieves the unique name of the tuning space.

## -parameters

### -param Name [out]

Pointer to a variable that receives the unique name.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>