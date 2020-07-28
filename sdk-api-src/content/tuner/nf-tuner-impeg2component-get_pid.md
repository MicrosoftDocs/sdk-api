---
UID: NF:tuner.IMPEG2Component.get_PID
title: IMPEG2Component::get_PID (tuner.h)
description: The get_PID method returns the packet identifier (PID) for this substream.
helpviewer_keywords: ["IMPEG2Component interface [Microsoft TV Technologies]","get_PID method","IMPEG2Component.get_PID","IMPEG2Component::get_PID","IMPEG2Componentget_PID","get_PID","get_PID method [Microsoft TV Technologies]","get_PID method [Microsoft TV Technologies]","IMPEG2Component interface","mstv.impeg2component_get_pid","tuner/IMPEG2Component::get_PID"]
old-location: mstv\impeg2component_get_pid.htm
tech.root: mstv
ms.assetid: 7d6b0b2f-fe48-4fc5-bb3b-639bb8ee2df8
ms.date: 12/05/2018
ms.keywords: IMPEG2Component interface [Microsoft TV Technologies],get_PID method, IMPEG2Component.get_PID, IMPEG2Component::get_PID, IMPEG2Componentget_PID, get_PID, get_PID method [Microsoft TV Technologies], get_PID method [Microsoft TV Technologies],IMPEG2Component interface, mstv.impeg2component_get_pid, tuner/IMPEG2Component::get_PID
f1_keywords:
- tuner/IMPEG2Component.get_PID
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- IMPEG2Component.get_PID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2Component::get_PID


## -description



The <b>get_PID</b> method returns the packet identifier (PID) for this substream.




## -parameters




### -param PID [out]

Pointer to a variable that receives the PID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component Interface</a>
 

 

