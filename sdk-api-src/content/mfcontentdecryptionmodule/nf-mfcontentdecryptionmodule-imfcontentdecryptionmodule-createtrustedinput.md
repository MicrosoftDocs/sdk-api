---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.CreateTrustedInput
title: IMFContentDecryptionModule::CreateTrustedInput
ms.date: 11/26/2019
targetos: Windows
description: Creates an IMFTrustedInput object that implements the decryption of content.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfcontentdecryptionmodule.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfcontentdecryptionmodule.h
api_name:
 - IMFContentDecryptionModule::CreateTrustedInput
f1_keywords:
 - IMFContentDecryptionModule::CreateTrustedInput
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::CreateTrustedInput
dev_langs:
 - c++
---

## -description

Creates an [IMFTrustedInput](../mfidl/nn-mfidl-imftrustedinput.md) object that implements the decryption of content.

## -parameters

### -param contentInitData

A **BYTE** array containing initialization data. *contentInitData* will only be used if initData from [IMFContentDecryptionModuleSession::GenerateRequest](nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession-generaterequest.md) is not provided or incomplete. Initialization Data should be structured in PSSH Box Format. For more details, see the Encrypted Media Extension specification's [Common SystemID and PSSH Box Format](https://www.w3.org/TR/eme-initdata-cenc/#common-system).

### -param contentInitDataSize

The size of the array in *contentInitData*.

### -param trustedInput

Receives the created **IMFTrustedInput** object.

## -returns

Returns S_OK on success.

## -remarks

An implementation of a Content Decryption Module (CDM) may include an implementation of [IMFInputTrustAuthority](../mfidl/nn-mfidl-imfinputtrustauthority.md) obtained by calling **CreateTrustedInput**.


The following attributes are supported for **IMFInputTrustAuthority** decrypter.

| Property                                      |Description
|-----------------------------------------------|---------------------------------------------------------------|
| [MFT_POLICY_SET_AWARE](/windows/win32/medfound/mft-policy-set-aware) | If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](/windows/win32/medfound/mepolicyset) completion notifications.|
| [MFT_USING_HARDWARE_DRM](/windows/win32/medfound/mft-using-hardware-drm) | Specifies whether the IMFTransform is using hardware DRM. If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM. If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM. If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM. |

## -see-also

[IMFTrustedInput](../mfidl/nn-mfidl-imftrustedinput.md)