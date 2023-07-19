---
UID: NF:tuner.IMPEG2Component.get_ProgramNumber
title: IMPEG2Component::get_ProgramNumber (tuner.h)
description: The get_ProgramNumber method returns the program number for this substream.
helpviewer_keywords: ["IMPEG2Component interface [Microsoft TV Technologies]","get_ProgramNumber method","IMPEG2Component.get_ProgramNumber","IMPEG2Component::get_ProgramNumber","IMPEG2Componentget_ProgramNumber","get_ProgramNumber","get_ProgramNumber method [Microsoft TV Technologies]","get_ProgramNumber method [Microsoft TV Technologies]","IMPEG2Component interface","mstv.impeg2component_get_programnumber","tuner/IMPEG2Component::get_ProgramNumber"]
old-location: mstv\impeg2component_get_programnumber.htm
tech.root: mstv
ms.assetid: a501c65d-26cf-44f4-b134-2a1080095eaa
ms.date: 12/05/2018
ms.keywords: IMPEG2Component interface [Microsoft TV Technologies],get_ProgramNumber method, IMPEG2Component.get_ProgramNumber, IMPEG2Component::get_ProgramNumber, IMPEG2Componentget_ProgramNumber, get_ProgramNumber, get_ProgramNumber method [Microsoft TV Technologies], get_ProgramNumber method [Microsoft TV Technologies],IMPEG2Component interface, mstv.impeg2component_get_programnumber, tuner/IMPEG2Component::get_ProgramNumber
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
 - IMPEG2Component::get_ProgramNumber
 - tuner/IMPEG2Component::get_ProgramNumber
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
 - IMPEG2Component.get_ProgramNumber
---

# IMPEG2Component::get_ProgramNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ProgramNumber</b> method returns the program number for this substream.

## -parameters

### -param ProgramNumber [out]

Pointer to a variable that receives the program number.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component Interface</a>