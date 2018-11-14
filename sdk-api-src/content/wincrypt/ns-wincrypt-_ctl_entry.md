---
UID: NS:wincrypt._CTL_ENTRY
title: "_CTL_ENTRY"
author: windows-sdk-content
description: An element of a certificate trust list (CTL).
old-location: security\ctl_entry.htm
tech.root: seccrypto
ms.assetid: ebc63847-b641-4205-b15c-7b32c1426c21
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCTL_ENTRY, CTL_ENTRY, CTL_ENTRY structure [Security], PCTL_ENTRY, PCTL_ENTRY structure pointer [Security], _CTL_ENTRY, _crypto2_ctl_entry, security.ctl_entry, wincrypt/CTL_ENTRY, wincrypt/PCTL_ENTRY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - CTL_ENTRY
product: Windows
targetos: Windows
req.typenames: CTL_ENTRY, *PCTL_ENTRY
req.redist: 
---

# _CTL_ENTRY structure


## -description


The <b>CTL_ENTRY</b> structure is an element of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL).


## -struct-fields




### -field SubjectIdentifier

<a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> containing a unique identifier of a subject. It can be a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> or any unique byte sequence.


### -field cAttribute

Count of elements in the <b>rgAttribute</b> member array.


### -field rgAttribute

Array of 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures, each holding information about the subject.


## -see-also




<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a>
 

 

