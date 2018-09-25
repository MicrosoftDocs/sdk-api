---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO
title: "_CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO"
author: windows-sdk-content
description: Contains information about the public key BLOB used by the CryptUIWizDigitalSign function.
old-location: security\cryptui_wiz_digital_sign_blob_info.htm
tech.root: seccrypto
ms.assetid: 9750f52a-f605-4f43-98e1-0f0ea947a214
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO structure [Security], PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO structure pointer [Security], _CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, security.cryptui_wiz_digital_sign_blob_info"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO
product: Windows
targetos: Windows
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO
req.redist: 
---

# _CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO</b> structure contains information about the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key BLOB</a> used by the <a href="https://msdn.microsoft.com/en-us/library/Aa380292(v=VS.85).aspx">CryptUIWizDigitalSign</a> function.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field pGuidSubject

A pointer to a <b>GUID</b> that contains the GUID that identifies the Session Initiation Protocol (SIP) functions to load.


### -field cbBlob

The size, in bytes, of the <a href="https://msdn.microsoft.com/en-us/library/ms721569(v=VS.85).aspx">BLOB</a> pointed to by the <b>pbBlob</b> member.


### -field pbBlob

A pointer to the BLOB to sign.


### -field pwszDisplayName

A pointer to a null-terminated Unicode string that contains the display name of the BLOB to sign.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380292(v=VS.85).aspx">CryptUIWizDigitalSign</a>
 

 

