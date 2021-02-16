---
UID: NS:mfidl._MFT_REGISTRATION_INFO
title: MFT_REGISTRATION_INFO (mfidl.h)
description: Contains parameters for the IMFLocalMFTRegistration::RegisterMFTs method.
helpviewer_keywords: ["MFT_REGISTRATION_INFO","MFT_REGISTRATION_INFO structure [Media Foundation]","mf.mft_registration_info","mfidl/MFT_REGISTRATION_INFO"]
old-location: mf\mft_registration_info.htm
tech.root: mf
ms.assetid: 7d610edf-89e3-4ff3-9ad8-b92ee50df522
ms.date: 12/05/2018
ms.keywords: MFT_REGISTRATION_INFO, MFT_REGISTRATION_INFO structure [Media Foundation], mf.mft_registration_info, mfidl/MFT_REGISTRATION_INFO
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFT_REGISTRATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_REGISTRATION_INFO
 - mfidl/_MFT_REGISTRATION_INFO
 - MFT_REGISTRATION_INFO
 - mfidl/MFT_REGISTRATION_INFO
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
 - MFT_REGISTRATION_INFO
---

# MFT_REGISTRATION_INFO structure


## -description

Contains parameters for the <a href="/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts">IMFLocalMFTRegistration::RegisterMFTs</a> method.

## -struct-fields

### -field clsid

CLSID of the Media Foundation transform (MFT) to register.

### -field guidCategory

GUID that specifies the category of the MFT. For a list of MFT categories, see <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.

### -field uiFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a> enumeration.

### -field pszName

Wide-character string that contains the friendly name of the MFT.

### -field cInTypes

Number of elements in the <b>pInTypes</b> array.

### -field pInTypes

Pointer to an array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array specifies an input format that the MFT supports. If this member is <b>NULL</b>, the <b>cInTypes</b> member must be zero.

### -field cOutTypes

Number of elements in the <b>pOutTypes</b> array.

### -field pOutTypes

Pointer to an array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array defines an output format that the MFT supports. If this member is <b>NULL</b>, the <b>cOutTypes</b> member must be zero.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>