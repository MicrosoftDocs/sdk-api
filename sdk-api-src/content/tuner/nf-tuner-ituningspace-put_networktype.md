---
UID: NF:tuner.ITuningSpace.put_NetworkType
title: ITuningSpace::put_NetworkType (tuner.h)
description: The put_NetworkType method specifies the network type of the tuning space as a BSTR.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","put_NetworkType method","ITuningSpace.put_NetworkType","ITuningSpace::put_NetworkType","ITuningSpaceput_NetworkType","mstv.ituningspace_put_networktype","put_NetworkType","put_NetworkType method [Microsoft TV Technologies]","put_NetworkType method [Microsoft TV Technologies]","ITuningSpace interface","tuner/ITuningSpace::put_NetworkType"]
old-location: mstv\ituningspace_put_networktype.htm
tech.root: mstv
ms.assetid: 6af7062c-41c9-447f-8d92-bd67b8348933
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_NetworkType method, ITuningSpace.put_NetworkType, ITuningSpace::put_NetworkType, ITuningSpaceput_NetworkType, mstv.ituningspace_put_networktype, put_NetworkType, put_NetworkType method [Microsoft TV Technologies], put_NetworkType method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_NetworkType
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
 - ITuningSpace::put_NetworkType
 - tuner/ITuningSpace::put_NetworkType
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
 - ITuningSpace.put_NetworkType
---

# ITuningSpace::put_NetworkType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_NetworkType</b> method specifies the network type of the tuning space as a <b>BSTR</b>.



This method is intended for Automation clients, because it specifies the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put__networktype">ITuningSpace::put__NetworkType</a> method instead, which takes a GUID value.

## -parameters

### -param NetworkTypeGuid [in]

Contains the string representation of the network type GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>