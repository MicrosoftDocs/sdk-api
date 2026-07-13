---
UID: NF:powersetting.PowerGetActiveScheme
title: PowerGetActiveScheme function (powersetting.h)
description: Retrieves the active power scheme and returns a GUID that identifies the scheme.
helpviewer_keywords: ["PowerGetActiveScheme","PowerGetActiveScheme function","base.powergetactivescheme","powersetting/PowerGetActiveScheme","powrprof/PowerGetActiveScheme"]
old-location: base\powergetactivescheme.htm
tech.root: base
ms.assetid: cd72562c-8987-40c1-89c7-04a95b5f1fd0
ms.date: 12/05/2018
ms.keywords: PowerGetActiveScheme, PowerGetActiveScheme function, base.powergetactivescheme, powersetting/PowerGetActiveScheme, powrprof/PowerGetActiveScheme
req.header: powersetting.h
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
 - PowerGetActiveScheme
 - powersetting/PowerGetActiveScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-power-setting-l1-1-1.dll
 - PowrProf.dll
 - API-MS-Win-power-setting-l1-1-0.dll
api_name:
 - PowerGetActiveScheme
---

# PowerGetActiveScheme function


## -description

Retrieves the active power scheme and returns a <b>GUID</b> that identifies the 
    scheme.

## -parameters

### -param UserRootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param ActivePolicyGuid [out]

A pointer that receives a pointer to a <b>GUID</b> structure. 
      Use the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to free this memory.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>