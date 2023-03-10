---
UID: NS:opmapi._OPM_HDCP_KEY_SELECTION_VECTOR
title: OPM_HDCP_KEY_SELECTION_VECTOR (opmapi.h)
description: Contains the key selection vector (KSV) for a High-Bandwidth Digital Content Protection (HDCP) receiver.
helpviewer_keywords: ["OPM_HDCP_KEY_SELECTION_VECTOR","OPM_HDCP_KEY_SELECTION_VECTOR structure [Media Foundation]","mf.opm_hdcp_key_selection_vector","opmapi/OPM_HDCP_KEY_SELECTION_VECTOR"]
old-location: mf\opm_hdcp_key_selection_vector.htm
tech.root: mf
ms.assetid: 79c0e5e5-62ef-4b8a-9e3b-3a9482731b16
ms.date: 12/05/2018
ms.keywords: OPM_HDCP_KEY_SELECTION_VECTOR, OPM_HDCP_KEY_SELECTION_VECTOR structure [Media Foundation], mf.opm_hdcp_key_selection_vector, opmapi/OPM_HDCP_KEY_SELECTION_VECTOR
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPM_HDCP_KEY_SELECTION_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_HDCP_KEY_SELECTION_VECTOR
 - opmapi/_OPM_HDCP_KEY_SELECTION_VECTOR
 - OPM_HDCP_KEY_SELECTION_VECTOR
 - opmapi/OPM_HDCP_KEY_SELECTION_VECTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_HDCP_KEY_SELECTION_VECTOR
---

# OPM_HDCP_KEY_SELECTION_VECTOR structure


## -description

Contains the key selection vector (KSV) for a High-Bandwidth Digital Content Protection (HDCP) receiver.

## -struct-fields

### -field abKeySelectionVector

A buffer that contains the device's KSV. (This is the value named <i>Bksv</i> in the HDCP specification.)

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/win32/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information">OPM_CONNECTED_HDCP_DEVICE_INFORMATION</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>