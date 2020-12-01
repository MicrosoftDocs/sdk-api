---
UID: NF:powrprof.PowerRestoreIndividualDefaultPowerScheme
title: PowerRestoreIndividualDefaultPowerScheme function (powrprof.h)
description: Replaces a specific power scheme for the current user with one from the default user (stored in HKEY_USERS\.Default).
helpviewer_keywords: ["PowerRestoreIndividualDefaultPowerScheme","PowerRestoreIndividualDefaultPowerScheme function","base.powerrestoreindividualdefaultpowerscheme","powrprof/PowerRestoreIndividualDefaultPowerScheme"]
old-location: base\powerrestoreindividualdefaultpowerscheme.htm
tech.root: base
ms.assetid: f1a9cfb1-1b56-4873-994b-7fe929fdc86c
ms.date: 12/05/2018
ms.keywords: PowerRestoreIndividualDefaultPowerScheme, PowerRestoreIndividualDefaultPowerScheme function, base.powerrestoreindividualdefaultpowerscheme, powrprof/PowerRestoreIndividualDefaultPowerScheme
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerRestoreIndividualDefaultPowerScheme
 - powrprof/PowerRestoreIndividualDefaultPowerScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerRestoreIndividualDefaultPowerScheme
---

# PowerRestoreIndividualDefaultPowerScheme function


## -description

Replaces a specific power scheme for the current user with one from the default user (stored in 
    <b>HKEY_USERS</b>&#92;<b>.Default</b>)

## -parameters

### -param SchemeGuid [in]

The identifier of the power scheme.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
	     the call failed.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>