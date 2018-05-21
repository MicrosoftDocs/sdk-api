---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO
title: "_CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO"
author: windows-driver-content
description: Contains information about the public key BLOB used by the CryptUIWizDigitalSign function.
old-location: security\cryptui_wiz_digital_sign_blob_info.htm
old-project: SecCrypto
ms.assetid: 9750f52a-f605-4f43-98e1-0f0ea947a214
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO structure [Security], PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO structure pointer [Security], _CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, security.cryptui_wiz_digital_sign_blob_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cryptuiapi.h
api_name:
-	CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO</b> structure contains information about the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a> used by the <a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a> function.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field pGuidSubject

A pointer to a <b>GUID</b> that contains the GUID that identifies the Session Initiation Protocol (SIP) functions to load.


### -field cbBlob

The size, in bytes, of the <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> pointed to by the <b>pbBlob</b> member.


### -field pbBlob

A pointer to the BLOB to sign.


### -field pwszDisplayName

A pointer to a null-terminated Unicode string that contains the display name of the BLOB to sign.


## -see-also




<a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a>
 

 

