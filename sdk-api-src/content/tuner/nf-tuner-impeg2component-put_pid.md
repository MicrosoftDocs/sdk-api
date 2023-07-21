---
UID: NF:tuner.IMPEG2Component.put_PID
title: IMPEG2Component::put_PID (tuner.h)
description: The put_PID method sets the packet identifier (PID) for this substream.
helpviewer_keywords: ["IMPEG2Component interface [Microsoft TV Technologies]","put_PID method","IMPEG2Component.put_PID","IMPEG2Component::put_PID","IMPEG2Componentput_PID","mstv.impeg2component_put_pid","put_PID","put_PID method [Microsoft TV Technologies]","put_PID method [Microsoft TV Technologies]","IMPEG2Component interface","tuner/IMPEG2Component::put_PID"]
old-location: mstv\impeg2component_put_pid.htm
tech.root: mstv
ms.assetid: 0bc19b79-1586-470d-85d5-3ef1babe60e2
ms.date: 12/05/2018
ms.keywords: IMPEG2Component interface [Microsoft TV Technologies],put_PID method, IMPEG2Component.put_PID, IMPEG2Component::put_PID, IMPEG2Componentput_PID, mstv.impeg2component_put_pid, put_PID, put_PID method [Microsoft TV Technologies], put_PID method [Microsoft TV Technologies],IMPEG2Component interface, tuner/IMPEG2Component::put_PID
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
 - IMPEG2Component::put_PID
 - tuner/IMPEG2Component::put_PID
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
 - IMPEG2Component.put_PID
---

# IMPEG2Component::put_PID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_PID</b> method sets the packet identifier (PID) for this substream.

## -parameters

### -param PID [in]

Specifies the PID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component Interface</a>