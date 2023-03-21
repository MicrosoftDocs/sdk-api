---
UID: NE:mfidl._MFNetCredentialOptions
title: MFNetCredentialOptions (mfidl.h)
description: Describes options for the caching network credentials.
helpviewer_keywords: ["5ee4f46c-762c-4acf-86ff-da7a93b5de05","MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT","MFNET_CREDENTIAL_DONT_CACHE","MFNET_CREDENTIAL_SAVE","MFNetCredentialOptions","MFNetCredentialOptions enumeration [Media Foundation]","mf.mfnetcredentialoptions","mfidl/MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT","mfidl/MFNET_CREDENTIAL_DONT_CACHE","mfidl/MFNET_CREDENTIAL_SAVE","mfidl/MFNetCredentialOptions"]
old-location: mf\mfnetcredentialoptions.htm
tech.root: mf
ms.assetid: 5ee4f46c-762c-4acf-86ff-da7a93b5de05
ms.date: 12/05/2018
ms.keywords: 5ee4f46c-762c-4acf-86ff-da7a93b5de05, MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT, MFNET_CREDENTIAL_DONT_CACHE, MFNET_CREDENTIAL_SAVE, MFNetCredentialOptions, MFNetCredentialOptions enumeration [Media Foundation], mf.mfnetcredentialoptions, mfidl/MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT, mfidl/MFNET_CREDENTIAL_DONT_CACHE, mfidl/MFNET_CREDENTIAL_SAVE, mfidl/MFNetCredentialOptions
req.header: mfidl.h
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
req.typenames: MFNetCredentialOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFNetCredentialOptions
 - mfidl/_MFNetCredentialOptions
 - MFNetCredentialOptions
 - mfidl/MFNetCredentialOptions
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
 - MFNetCredentialOptions
---

# MFNetCredentialOptions enumeration


## -description

Describes options for the caching network credentials.

## -enum-fields

### -field MFNET_CREDENTIAL_SAVE:0x1

Allow the credential cache object to save credentials in persistent storage.

### -field MFNET_CREDENTIAL_DONT_CACHE:0x2

Do not allow the credential cache object to cache the credentials in memory. This flag cannot be combined with the MFNET_CREDENTIAL_SAVE flag.

### -field MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT:0x4

The user allows credentials to be sent over the network in clear text.

 By default, <a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential">IMFNetCredentialCache::GetCredential</a> always returns the REQUIRE_PROMPT flag when the authentication flags include MFNET_AUTHENTICATION_CLEAR_TEXT, even if cached credentials are available. If you set the MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT option, the <b>GetCredential</b> method will not return  REQUIRE_PROMPT for clear text, if cached credentials are available.

Do not set this flag without notifying the user that credentials might be sent in clear text.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions">IMFNetCredentialCache::SetUserOptions</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/network-source-authentication">Network Source Authentication</a>
