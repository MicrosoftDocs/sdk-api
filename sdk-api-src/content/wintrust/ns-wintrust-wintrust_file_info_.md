---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

