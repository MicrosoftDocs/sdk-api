---
UID: NS:ksopmapi._OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
title: OPM_ENCRYPTED_INITIALIZATION_PARAMETERS (ksopmapi.h)
description: The OPM_ENCRYPTED_INITIALIZATION_PARAMETERS (ksopmapi.h) structure contains initialization parameters for an Output Protection Manager (OPM) session.
helpviewer_keywords: ["OPM_ENCRYPTED_INITIALIZATION_PARAMETERS","OPM_ENCRYPTED_INITIALIZATION_PARAMETERS structure [Media Foundation]","_OPM_ENCRYPTED_INITIALIZATION_PARAMETERS","ksopmapi/OPM_ENCRYPTED_INITIALIZATION_PARAMETERS","mf.opm_encrypted_initialization_parameters"]
old-location: mf\opm_encrypted_initialization_parameters.htm
tech.root: mf
ms.assetid: abcf0b84-7370-48da-b4dd-4faded6be343
ms.date: 08/05/2022
ms.keywords: OPM_ENCRYPTED_INITIALIZATION_PARAMETERS, OPM_ENCRYPTED_INITIALIZATION_PARAMETERS structure [Media Foundation], _OPM_ENCRYPTED_INITIALIZATION_PARAMETERS, ksopmapi/OPM_ENCRYPTED_INITIALIZATION_PARAMETERS, mf.opm_encrypted_initialization_parameters
req.header: ksopmapi.h
req.include-header: Opmapi.h
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
req.typenames: OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
 - ksopmapi/_OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
 - OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
 - ksopmapi/OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_ENCRYPTED_INITIALIZATION_PARAMETERS
---

# OPM_ENCRYPTED_INITIALIZATION_PARAMETERS structure


## -description

Contains initialization parameters for an <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) session.

## -struct-fields

### -field abEncryptedInitializationParameters

Pointer to a buffer that contains encrypted initialization parameters for the session. For more information, see <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization">IOPMVideoOutput::FinishInitialization</a>.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/strmif/ns-strmif-amcoppsignature">AMCOPPSignature</a> structure used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
