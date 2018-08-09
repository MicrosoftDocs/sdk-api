---
UID: NS:winsafer._SAFER_PATHNAME_IDENTIFICATION
title: "_SAFER_PATHNAME_IDENTIFICATION"
author: windows-sdk-content
description: Represents a path identification rule.
old-location: security\safer_pathname_identification.htm
old-project: secmgmt
ms.assetid: d845a750-2931-4c17-be78-92843e2bd76f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSAFER_PATHNAME_IDENTIFICATION, PSAFER_PATHNAME_IDENTIFICATION, PSAFER_PATHNAME_IDENTIFICATION structure pointer [Security], SAFER_PATHNAME_IDENTIFICATION, SAFER_PATHNAME_IDENTIFICATION structure [Security], _SAFER_PATHNAME_IDENTIFICATION, _mnp_safer_pathname_identification, security.safer_pathname_identification, winsafer/PSAFER_PATHNAME_IDENTIFICATION, winsafer/SAFER_PATHNAME_IDENTIFICATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsafer.h
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
tech.root: 
req.typenames: SAFER_PATHNAME_IDENTIFICATION, *PSAFER_PATHNAME_IDENTIFICATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_PATHNAME_IDENTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SAFER_PATHNAME_IDENTIFICATION structure


## -description


The <b>SAFER_PATHNAME_IDENTIFICATION</b> structure represents a path identification rule.


## -struct-fields




### -field header

A  <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure containing the structure header. The <b>dwIdentificationType</b> member of the header must be <b>SaferIdentityTypeImageName</b>, and the  <b>cbStructSize</b> member of the header must be sizeof(SAFER_PATHNAME_IDENTIFICATION).


### -field Description

A description of the path identification rule provided by the user.


### -field ImageName

A pointer to a <b>null</b>-terminated wide character string that specifies the fully qualified path and file name to be used for path-based discrimination checks. The image name is also used to open and read the file to identify any other discrimination criteria not supplied in this structure. This member can be set to <b>NULL</b>. If the <b>dwCheckFlags</b> member of the <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure specified by the <b>header</b> member includes SAFER_CRITERIA_AUTHENTICODE, either the <b>hImageFileHandle</b> member or the <b>ImagePath</b> member of the <b>SAFER_IDENTIFICATION_HEADER</b> structure must be set.


### -field dwSaferFlags

Reserved for future use.

