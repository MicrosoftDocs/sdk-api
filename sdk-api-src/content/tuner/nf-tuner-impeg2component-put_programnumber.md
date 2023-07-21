---
UID: NF:tuner.IMPEG2Component.put_ProgramNumber
title: IMPEG2Component::put_ProgramNumber (tuner.h)
description: The put_ProgramNumber method sets the program number for this substream.
helpviewer_keywords: ["IMPEG2Component interface [Microsoft TV Technologies]","put_ProgramNumber method","IMPEG2Component.put_ProgramNumber","IMPEG2Component::put_ProgramNumber","IMPEG2Componentput_ProgramNumber","mstv.impeg2component_put_programnumber","put_ProgramNumber","put_ProgramNumber method [Microsoft TV Technologies]","put_ProgramNumber method [Microsoft TV Technologies]","IMPEG2Component interface","tuner/IMPEG2Component::put_ProgramNumber"]
old-location: mstv\impeg2component_put_programnumber.htm
tech.root: mstv
ms.assetid: f8bc605f-6e3f-427c-a91e-2d4cbb59b65e
ms.date: 12/05/2018
ms.keywords: IMPEG2Component interface [Microsoft TV Technologies],put_ProgramNumber method, IMPEG2Component.put_ProgramNumber, IMPEG2Component::put_ProgramNumber, IMPEG2Componentput_ProgramNumber, mstv.impeg2component_put_programnumber, put_ProgramNumber, put_ProgramNumber method [Microsoft TV Technologies], put_ProgramNumber method [Microsoft TV Technologies],IMPEG2Component interface, tuner/IMPEG2Component::put_ProgramNumber
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
 - IMPEG2Component::put_ProgramNumber
 - tuner/IMPEG2Component::put_ProgramNumber
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
 - IMPEG2Component.put_ProgramNumber
---

# IMPEG2Component::put_ProgramNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_ProgramNumber</b> method sets the program number for this substream.

## -parameters

### -param ProgramNumber [in]

Specifies the program number.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component Interface</a>