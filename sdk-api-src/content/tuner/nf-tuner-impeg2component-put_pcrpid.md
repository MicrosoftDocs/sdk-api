---
UID: NF:tuner.IMPEG2Component.put_PCRPID
title: IMPEG2Component::put_PCRPID (tuner.h)
description: The put_PCRPID method sets the packet identifier (PID) for the packets that contain the PCR for this substream.
helpviewer_keywords: ["IMPEG2Component interface [Microsoft TV Technologies]","put_PCRPID method","IMPEG2Component.put_PCRPID","IMPEG2Component::put_PCRPID","IMPEG2Componentput_PCRPID","mstv.impeg2component_put_pcrpid","put_PCRPID","put_PCRPID method [Microsoft TV Technologies]","put_PCRPID method [Microsoft TV Technologies]","IMPEG2Component interface","tuner/IMPEG2Component::put_PCRPID"]
old-location: mstv\impeg2component_put_pcrpid.htm
tech.root: mstv
ms.assetid: cfe55ec9-cf07-40c5-98da-cb23393490d0
ms.date: 12/05/2018
ms.keywords: IMPEG2Component interface [Microsoft TV Technologies],put_PCRPID method, IMPEG2Component.put_PCRPID, IMPEG2Component::put_PCRPID, IMPEG2Componentput_PCRPID, mstv.impeg2component_put_pcrpid, put_PCRPID, put_PCRPID method [Microsoft TV Technologies], put_PCRPID method [Microsoft TV Technologies],IMPEG2Component interface, tuner/IMPEG2Component::put_PCRPID
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
 - IMPEG2Component::put_PCRPID
 - tuner/IMPEG2Component::put_PCRPID
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
 - IMPEG2Component.put_PCRPID
---

# IMPEG2Component::put_PCRPID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_PCRPID</b> method sets the packet identifier (PID) for the packets that contain the PCR for this substream.

## -parameters

### -param PCRPID [in]

Specifies the PCR PID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component Interface</a>