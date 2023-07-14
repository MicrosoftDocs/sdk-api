---
UID: NF:tuner.ITuningSpace.get_FriendlyName
title: ITuningSpace::get_FriendlyName (tuner.h)
description: The get_FriendlyName method retrieves the localized, user-friendly name of the tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_FriendlyName method","ITuningSpace.get_FriendlyName","ITuningSpace::get_FriendlyName","ITuningSpaceget_FriendlyName","get_FriendlyName","get_FriendlyName method [Microsoft TV Technologies]","get_FriendlyName method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_friendlyname","tuner/ITuningSpace::get_FriendlyName"]
old-location: mstv\ituningspace_get_friendlyname.htm
tech.root: mstv
ms.assetid: d1427aae-49e9-45ce-abd9-902a895e6e44
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_FriendlyName method, ITuningSpace.get_FriendlyName, ITuningSpace::get_FriendlyName, ITuningSpaceget_FriendlyName, get_FriendlyName, get_FriendlyName method [Microsoft TV Technologies], get_FriendlyName method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_friendlyname, tuner/ITuningSpace::get_FriendlyName
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
 - ITuningSpace::get_FriendlyName
 - tuner/ITuningSpace::get_FriendlyName
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
 - ITuningSpace.get_FriendlyName
---

# ITuningSpace::get_FriendlyName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FriendlyName</b> method retrieves the localized, user-friendly name of the tuning space.

## -parameters

### -param Name [out]

Pointer to a variable receives the user-friendly name.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>