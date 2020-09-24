---
UID: NS:mfidl._MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
title: MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS (mfidl.h)
description: Contains parameters for the IMFInputTrustAuthority::BindAccess or IMFInputTrustAuthority::UpdateAccess method.
helpviewer_keywords: ["5ff3ec3a-a7b1-4378-8e8b-d59a6f5bb28d","MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS","MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS structure [Media Foundation]","mf.mfinputtrustauthority_access_params","mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS"]
old-location: mf\mfinputtrustauthority_access_params.htm
tech.root: mf
ms.assetid: 5ff3ec3a-a7b1-4378-8e8b-d59a6f5bb28d
ms.date: 12/05/2018
ms.keywords: 5ff3ec3a-a7b1-4378-8e8b-d59a6f5bb28d, MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS, MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS structure [Media Foundation], mf.mfinputtrustauthority_access_params, mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
 - mfidl/_MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
 - MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
 - mfidl/MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS
---

# MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS structure


## -description

Contains parameters for the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-bindaccess">IMFInputTrustAuthority::BindAccess</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-updateaccess">IMFInputTrustAuthority::UpdateAccess</a> method.

## -struct-fields

### -field dwSize

Size of the structure, in bytes.

### -field dwVer

Version number. This value must be zero.

### -field cbSignatureOffset

Offset of the signature from the start of the structure, in bytes.

### -field cbSignatureSize

Size of the signature, in bytes.

### -field cbExtensionOffset

Offset of the extension blob from the start of the structure, in bytes.

### -field cbExtensionSize

Size of the extension blob, in bytes.

### -field cActions

Number of elements in the <b>rgOutputActions</b> array.

### -field rgOutputActions

Array of <a href="/windows/win32/api/mfidl/ns-mfidl-mfinputtrustauthority_access_action">MFINPUTTRUSTAUTHORITY_ACCESS_ACTION</a> structures. The number of elements in the array is specified in the <b>cActions</b> member.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>