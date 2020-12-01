---
UID: NS:winsafer._SAFER_PATHNAME_IDENTIFICATION
title: SAFER_PATHNAME_IDENTIFICATION (winsafer.h)
description: Represents a path identification rule.
helpviewer_keywords: ["*PSAFER_PATHNAME_IDENTIFICATION","PSAFER_PATHNAME_IDENTIFICATION","PSAFER_PATHNAME_IDENTIFICATION structure pointer [Security]","SAFER_PATHNAME_IDENTIFICATION","SAFER_PATHNAME_IDENTIFICATION structure [Security]","_mnp_safer_pathname_identification","security.safer_pathname_identification","winsafer/PSAFER_PATHNAME_IDENTIFICATION","winsafer/SAFER_PATHNAME_IDENTIFICATION"]
old-location: security\safer_pathname_identification.htm
tech.root: security
ms.assetid: d845a750-2931-4c17-be78-92843e2bd76f
ms.date: 12/05/2018
ms.keywords: '*PSAFER_PATHNAME_IDENTIFICATION, PSAFER_PATHNAME_IDENTIFICATION, PSAFER_PATHNAME_IDENTIFICATION structure pointer [Security], SAFER_PATHNAME_IDENTIFICATION, SAFER_PATHNAME_IDENTIFICATION structure [Security], _mnp_safer_pathname_identification, security.safer_pathname_identification, winsafer/PSAFER_PATHNAME_IDENTIFICATION, winsafer/SAFER_PATHNAME_IDENTIFICATION'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SAFER_PATHNAME_IDENTIFICATION, *PSAFER_PATHNAME_IDENTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_PATHNAME_IDENTIFICATION
 - winsafer/_SAFER_PATHNAME_IDENTIFICATION
 - PSAFER_PATHNAME_IDENTIFICATION
 - winsafer/PSAFER_PATHNAME_IDENTIFICATION
 - SAFER_PATHNAME_IDENTIFICATION
 - winsafer/SAFER_PATHNAME_IDENTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_PATHNAME_IDENTIFICATION
---

# SAFER_PATHNAME_IDENTIFICATION structure


## -description

The <b>SAFER_PATHNAME_IDENTIFICATION</b> structure represents a path identification rule.

## -struct-fields

### -field header

A  <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_identification_header">SAFER_IDENTIFICATION_HEADER</a> structure containing the structure header. The <b>dwIdentificationType</b> member of the header must be <b>SaferIdentityTypeImageName</b>, and the  <b>cbStructSize</b> member of the header must be sizeof(SAFER_PATHNAME_IDENTIFICATION).

### -field Description

A description of the path identification rule provided by the user.

### -field ImageName

A pointer to a <b>null</b>-terminated wide character string that specifies the fully qualified path and file name to be used for path-based discrimination checks. The image name is also used to open and read the file to identify any other discrimination criteria not supplied in this structure. This member can be set to <b>NULL</b>. If the <b>dwCheckFlags</b> member of the <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_identification_header">SAFER_IDENTIFICATION_HEADER</a> structure specified by the <b>header</b> member includes SAFER_CRITERIA_AUTHENTICODE, either the <b>hImageFileHandle</b> member or the <b>ImagePath</b> member of the <b>SAFER_IDENTIFICATION_HEADER</b> structure must be set.

### -field dwSaferFlags

Reserved for future use.