---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_OPM_STATUS
title: MF_MEDIA_ENGINE_OPM_STATUS (mfmediaengine.h)
description: Defines the status of the Output Protection Manager (OPM).
helpviewer_keywords: ["MF_MEDIA_ENGINE_OPM_ESTABLISHED","MF_MEDIA_ENGINE_OPM_FAILED","MF_MEDIA_ENGINE_OPM_FAILED_BDA","MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER","MF_MEDIA_ENGINE_OPM_FAILED_VM","MF_MEDIA_ENGINE_OPM_NOT_REQUESTED","MF_MEDIA_ENGINE_OPM_STATUS","MF_MEDIA_ENGINE_OPM_STATUS enumeration [Media Foundation]","mf.mf_media_engine_opm_status","mfmediaengine/MF_MEDIA_ENGINE_OPM_ESTABLISHED","mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED","mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_BDA","mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER","mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_VM","mfmediaengine/MF_MEDIA_ENGINE_OPM_NOT_REQUESTED","mfmediaengine/MF_MEDIA_ENGINE_OPM_STATUS"]
old-location: mf\mf_media_engine_opm_status.htm
tech.root: mf
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_OPM_ESTABLISHED, MF_MEDIA_ENGINE_OPM_FAILED, MF_MEDIA_ENGINE_OPM_FAILED_BDA, MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER, MF_MEDIA_ENGINE_OPM_FAILED_VM, MF_MEDIA_ENGINE_OPM_NOT_REQUESTED, MF_MEDIA_ENGINE_OPM_STATUS, MF_MEDIA_ENGINE_OPM_STATUS enumeration [Media Foundation], mf.mf_media_engine_opm_status, mfmediaengine/MF_MEDIA_ENGINE_OPM_ESTABLISHED, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_BDA, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER, mfmediaengine/MF_MEDIA_ENGINE_OPM_FAILED_VM, mfmediaengine/MF_MEDIA_ENGINE_OPM_NOT_REQUESTED, mfmediaengine/MF_MEDIA_ENGINE_OPM_STATUS
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_OPM_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_OPM_STATUS
 - mfmediaengine/MF_MEDIA_ENGINE_OPM_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_OPM_STATUS
---

# MF_MEDIA_ENGINE_OPM_STATUS enumeration


## -description

Defines the status of the <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>  (OPM).

## -enum-fields

### -field MF_MEDIA_ENGINE_OPM_NOT_REQUESTED:0

Default status. Used to return the correct status when the content is unprotected.

### -field MF_MEDIA_ENGINE_OPM_ESTABLISHED:1

OPM successfully established.

### -field MF_MEDIA_ENGINE_OPM_FAILED_VM:2

OPM failed because running in a virtual machined (VM).

### -field MF_MEDIA_ENGINE_OPM_FAILED_BDA:3

OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).

### -field MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER:4

OPM failed because the graphics 
driver is not PE signed, falling back to WARP.

### -field MF_MEDIA_ENGINE_OPM_FAILED:5

OPM failed for other reasons.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
