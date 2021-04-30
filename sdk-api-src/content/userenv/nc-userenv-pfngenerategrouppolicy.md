---
UID: NC:userenv.PFNGENERATEGROUPPOLICY
title: PFNGENERATEGROUPPOLICY (userenv.h)
description: The GenerateGroupPolicy callback function is an application-defined callback function that each policy extension must export when generating RSoP data in the planning mode.
helpviewer_keywords: ["GPO_INFO_FLAG_SLOWLINK","GPO_INFO_FLAG_VERBOSE","GenerateGroupPolicy","PFNGENERATEGROUPPOLICY","PFNGENERATEGROUPPOLICY callback","PFNGENERATEGROUPPOLICY callback function [Group Policy]","_win32_generategrouppolicy","policy.generategrouppolicy","userenv/PFNGENERATEGROUPPOLICY"]
old-location: policy\generategrouppolicy.htm
tech.root: Policy
ms.assetid: 748b61a1-79fb-44b9-8c9b-0b1746fa981b
ms.date: 12/05/2018
ms.keywords: GPO_INFO_FLAG_SLOWLINK, GPO_INFO_FLAG_VERBOSE, GenerateGroupPolicy, PFNGENERATEGROUPPOLICY, PFNGENERATEGROUPPOLICY callback, PFNGENERATEGROUPPOLICY callback function [Group Policy], _win32_generategrouppolicy, policy.generategrouppolicy, userenv/PFNGENERATEGROUPPOLICY
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNGENERATEGROUPPOLICY
 - userenv/PFNGENERATEGROUPPOLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Userenv.h
api_name:
 - PFNGENERATEGROUPPOLICY
---

# PFNGENERATEGROUPPOLICY callback function


## -description

The
    <b>GenerateGroupPolicy</b> callback function is an application-defined callback function that each policy extension must export when generating RSoP data in the planning mode. The Group Policy Data Access Service (GPDAS) calls the function after the service simulates the loading of client-side extensions so that extensions can generate policy data.

The <b>PFNGENERATEGROUPPOLICY</b> type defines a pointer to this callback function. 
<b>GenerateGroupPolicy</b> is a placeholder for the application-defined function name.

## -parameters

### -param dwFlags [in]

A parameter that represents one or more of the following flags.



#### GPO_INFO_FLAG_SLOWLINK

The policy is applied across a slow link.



#### GPO_INFO_FLAG_VERBOSE

Write verbose output to the event log.

### -param pbAbort [in]

A value that specifies whether to continue processing GPOs. If this parameter is <b>TRUE</b>, GPO processing stops and the extension must deallocate its resources and return promptly. If this parameter is <b>FALSE</b>, GPO processing continues.

### -param pwszSite [in]

A pointer to the site name of the target computer. This parameter can be <b>NULL</b>.

### -param pComputerTarget [in]

A pointer to an 
<a href="/windows/desktop/api/userenv/ns-userenv-rsop_target">RSOP_TARGET</a> structure that contains information about a computer. This parameter can be <b>NULL</b>, but if it is <b>NULL</b>, the <i>pUserTarget</i> parameter is required.

### -param pUserTarget [in]

A pointer to an 
<a href="/windows/desktop/api/userenv/ns-userenv-rsop_target">RSOP_TARGET</a> structure that contains information about a user. This parameter can be <b>NULL</b>, but if it is <b>NULL</b>, the <i>pComputerTarget</i> parameter is required.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

The policy extension must register this callback function at the registry key:<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows NT</b>&#92;<b>CurrentVersion</b>&#92;<b>Winlogon</b>&#92;<b>GPExtensions</b>&#92;<b>ClientExtensionGuid</b>



<b>GenerateGroupPolicy</b>
<b>REG_SZ</b>

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/ns-userenv-rsop_target">RSOP_TARGET</a>
