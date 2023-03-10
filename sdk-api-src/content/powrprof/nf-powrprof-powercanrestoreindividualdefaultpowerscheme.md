---
UID: NF:powrprof.PowerCanRestoreIndividualDefaultPowerScheme
title: PowerCanRestoreIndividualDefaultPowerScheme function (powrprof.h)
description: Determines if the current user has access to the data for the specified power scheme so that it could be restored if necessary.
helpviewer_keywords: ["PowerCanRestoreIndividualDefaultPowerScheme","PowerCanRestoreIndividualDefaultPowerScheme function","base.powercanrestoreindividualdefaultpowerscheme","powrprof/PowerCanRestoreIndividualDefaultPowerScheme"]
old-location: base\powercanrestoreindividualdefaultpowerscheme.htm
tech.root: base
ms.assetid: 8f29c993-b237-4302-a48b-05368ead9a44
ms.date: 12/05/2018
ms.keywords: PowerCanRestoreIndividualDefaultPowerScheme, PowerCanRestoreIndividualDefaultPowerScheme function, base.powercanrestoreindividualdefaultpowerscheme, powrprof/PowerCanRestoreIndividualDefaultPowerScheme
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
 - PowerCanRestoreIndividualDefaultPowerScheme
 - powrprof/PowerCanRestoreIndividualDefaultPowerScheme
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
 - PowerCanRestoreIndividualDefaultPowerScheme
---

# PowerCanRestoreIndividualDefaultPowerScheme function


## -description

Determines if the current user has access to the data for the specified power scheme so that it could 
    be restored if necessary.

## -parameters

### -param SchemeGuid [in]

The identifier of the power scheme.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>