---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO
title: "_CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO"
author: windows-sdk-content
description: Used with the CRYPTUI_WIZ_DIGITAL_SIGN_INFO structure to contain information about the PVK file used by the digital signature wizard.
old-location: security\cryptui_wiz_digital_sign_pvk_file_info.htm
tech.root: seccrypto
ms.assetid: 0e737661-2cc3-47be-ab32-0efbc18fefbd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO structure [Security], PCRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO structure pointer [Security], _CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, security.cryptui_wiz_digital_sign_pvk_file_info"
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
 - CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO
product: Windows
targetos: Windows
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO
req.redist: 
---

# _CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/22d0bc45-0f66-4f5f-87d3-0849c4327eed">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a> structure to contain information about the PVK file used by the digital signature wizard.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field pwszPvkFileName

A pointer to a null-terminated Unicode string that contains the path and file name of the PVK file.


### -field pwszProvName

A pointer to a null-terminated Unicode string that contains the name of the provider.


### -field dwProvType

Contains the provider type identifier. For more information about the provider types, see <a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>.


## -see-also




<a href="https://msdn.microsoft.com/22d0bc45-0f66-4f5f-87d3-0849c4327eed">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a>



<a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>
 

 

