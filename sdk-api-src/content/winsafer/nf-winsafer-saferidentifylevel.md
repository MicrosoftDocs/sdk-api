---
UID: NF:winsafer.SaferIdentifyLevel
title: SaferIdentifyLevel function (winsafer.h)
description: Retrieves information about a level.
helpviewer_keywords: ["SaferIdentifyLevel","SaferIdentifyLevel function [Security]","_mnp_saferidentifylevel","security.saferidentifylevel","winsafer/SaferIdentifyLevel"]
old-location: security\saferidentifylevel.htm
tech.root: security
ms.assetid: f82c4f40-5c37-4f97-95a2-4b2cc26bf41e
ms.date: 12/05/2018
ms.keywords: SaferIdentifyLevel, SaferIdentifyLevel function [Security], _mnp_saferidentifylevel, security.saferidentifylevel, winsafer/SaferIdentifyLevel
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaferIdentifyLevel
 - winsafer/SaferIdentifyLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
api_name:
 - SaferIdentifyLevel
req.apiset: ext-ms-win-advapi32-safer-l1-1-0 (introduced in Windows 8)
---

# SaferIdentifyLevel function


## -description

The <b>SaferIdentifyLevel</b> function retrieves information about a level.

## -parameters

### -param dwNumProperties [in]

Number of 
<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_code_properties_v2">SAFER_CODE_PROPERTIES</a> structures in the <i>pCodeproperties</i>  parameter.

### -param pCodeProperties [in, optional]

Array of <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_code_properties_v2">SAFER_CODE_PROPERTIES</a> structures. Each structure contains a code file to be checked and the  criteria used to check the file.

### -param pLevelHandle [out]

The returned SAFER_LEVEL_HANDLE. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/winsafer/nf-winsafer-safercloselevel">SaferCloseLevel</a> function.

### -param lpReserved

Reserved for future use. Should be set to <b>NULL</b>.

Beginning with Windows 8 and Windows Server 2012 SRP_POLICY_APPX is defined as Windows Store app.

## -returns

<b>TRUE</b> if a SAFER_LEVEL_HANDLE was opened; otherwise,  <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
