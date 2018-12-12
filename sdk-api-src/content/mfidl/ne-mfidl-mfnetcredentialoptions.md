---
UID: NE:mfidl._MFNetCredentialOptions
title: MFNetCredentialOptions
author: windows-sdk-content
description: Describes options for the caching network credentials.
old-location: mf\mfnetcredentialoptions.htm
tech.root: medfound
ms.assetid: 5ee4f46c-762c-4acf-86ff-da7a93b5de05
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5ee4f46c-762c-4acf-86ff-da7a93b5de05, MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT, MFNET_CREDENTIAL_DONT_CACHE, MFNET_CREDENTIAL_SAVE, MFNetCredentialOptions, MFNetCredentialOptions enumeration [Media Foundation], mf.mfnetcredentialoptions, mfidl/MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT, mfidl/MFNET_CREDENTIAL_DONT_CACHE, mfidl/MFNET_CREDENTIAL_SAVE, mfidl/MFNetCredentialOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFNetCredentialOptions
product: Windows
targetos: Windows
req.typenames: MFNetCredentialOptions
req.redist: 
---

# MFNetCredentialOptions enumeration


## -description



Describes options for the caching network credentials.




## -enum-fields




### -field MFNET_CREDENTIAL_SAVE

Allow the credential cache object to save  credentials in persistant storage.


### -field MFNET_CREDENTIAL_DONT_CACHE

Do not allow the credential cache object to cache the credentials in memory. This flag cannot be combined with the MFNET_CREDENTIAL_SAVE flag.


### -field MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT

The user allows credentials to be sent over the network in clear text.

 By default, <a href="https://msdn.microsoft.com/7e095445-354a-4fbb-b354-bf87eb77552f">IMFNetCredentialCache::GetCredential</a> always returns the REQUIRE_PROMPT flag when the authentication flags include MFNET_AUTHENTICATION_CLEAR_TEXT, even if cached credentials are available. If you set the MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT option, the <b>GetCredential</b> method will not return  REQUIRE_PROMPT for clear text, if cached credentials are available.

Do not set this flag without notifying the user that credentials might be sent in clear text.


## -see-also




<a href="https://msdn.microsoft.com/024eea57-e7c8-495d-9959-ab37dd45873d">IMFNetCredentialCache::SetUserOptions</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

