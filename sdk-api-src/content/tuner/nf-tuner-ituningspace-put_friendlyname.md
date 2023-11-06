---
UID: NF:tuner.ITuningSpace.put_FriendlyName
title: ITuningSpace::put_FriendlyName (tuner.h)
description: The put_FriendlyName method sets the localized, user-friendly name of the tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","put_FriendlyName method","ITuningSpace.put_FriendlyName","ITuningSpace::put_FriendlyName","ITuningSpaceput_FriendlyName","mstv.ituningspace_put_friendlyname","put_FriendlyName","put_FriendlyName method [Microsoft TV Technologies]","put_FriendlyName method [Microsoft TV Technologies]","ITuningSpace interface","tuner/ITuningSpace::put_FriendlyName"]
old-location: mstv\ituningspace_put_friendlyname.htm
tech.root: mstv
ms.assetid: 97457657-9d28-4c8e-9db6-61271aa127e3
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_FriendlyName method, ITuningSpace.put_FriendlyName, ITuningSpace::put_FriendlyName, ITuningSpaceput_FriendlyName, mstv.ituningspace_put_friendlyname, put_FriendlyName, put_FriendlyName method [Microsoft TV Technologies], put_FriendlyName method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_FriendlyName
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
 - ITuningSpace::put_FriendlyName
 - tuner/ITuningSpace::put_FriendlyName
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
 - ITuningSpace.put_FriendlyName
---

# ITuningSpace::put_FriendlyName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_FriendlyName</b> method sets the localized, user-friendly name of the tuning space.

## -parameters

### -param Name [in]

Specifies the user-friendly name.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>