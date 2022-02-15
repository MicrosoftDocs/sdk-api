---
UID: NF:powrprof.PowerRestoreDefaultPowerSchemes
title: PowerRestoreDefaultPowerSchemes function (powrprof.h)
description: Replaces the power schemes for the system with default power schemes. All current power schemes and settings are deleted and replaced with the default system power schemes.
helpviewer_keywords: ["PowerRestoreDefaultPowerSchemes","PowerRestoreDefaultPowerSchemes function","base.powerrestoredefaultpowerschemes","powrprof/PowerRestoreDefaultPowerSchemes"]
old-location: base\powerrestoredefaultpowerschemes.htm
tech.root: base
ms.assetid: 6d0a6167-34de-439b-afb4-2536c715905c
ms.date: 12/05/2018
ms.keywords: PowerRestoreDefaultPowerSchemes, PowerRestoreDefaultPowerSchemes function, base.powerrestoredefaultpowerschemes, powrprof/PowerRestoreDefaultPowerSchemes
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
 - PowerRestoreDefaultPowerSchemes
 - powrprof/PowerRestoreDefaultPowerSchemes
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
 - PowerRestoreDefaultPowerSchemes
---

# PowerRestoreDefaultPowerSchemes function


## -description

Replaces the power schemes for the system with default power schemes. All current 
     power schemes and settings are deleted and replaced with the default system power schemes.



## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

## -remarks

The caller must be a member of the local Administrators group.

