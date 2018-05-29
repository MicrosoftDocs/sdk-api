---
UID: NS:wintrust.WINTRUST_FILE_INFO_
title: WINTRUST_FILE_INFO_
author: windows-sdk-content
description: The WINTRUST_FILE_INFO structure is used when calling WinVerifyTrust to verify an individual file.
old-location: security\wintrust_file_info.htm
old-project: SecCrypto
ms.assetid: 3c3bef86-a2ed-47d1-a726-90630433358a
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PWINTRUST_FILE_INFO, PWINTRUCT_FILE_INFO, PWINTRUCT_FILE_INFO structure pointer [Security], WINTRUST_FILE_INFO, WINTRUST_FILE_INFO structure [Security], WINTRUST_FILE_INFO_, _win32_wintrust_file_info, security.wintrust_file_info, wintrust/PWINTRUCT_FILE_INFO, wintrust/WINTRUST_FILE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
req.typenames: WINTRUST_FILE_INFO, *PWINTRUST_FILE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wintrust.h
api_name:
-	WINTRUST_FILE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WINTRUST_FILE_INFO_ structure


## -description



			The <b>WINTRUST_FILE_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify an individual file.


## -struct-fields




### -field cbStruct

Count of bytes in this structure.


### -field pcwszFilePath

Full path and file name of the file to be verified. This parameter cannot be <b>NULL</b>.


### -field hFile

Optional. File handle to the open file to be verified. This handle must be to a file that has at least read permission. This member can be set to <b>NULL</b>.


### -field pgKnownSubject

Optional. Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that specifies the subject type. This member can be set to <b>NULL</b>.

