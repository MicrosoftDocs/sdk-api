---
UID: NF:powersetting.PowerSetActiveScheme
title: PowerSetActiveScheme function (powersetting.h)
description: Sets the active power scheme for the current user.helpviewer_keywords: ["PowerSetActiveScheme","PowerSetActiveScheme function","base.powersetactivescheme","powersetting/PowerSetActiveScheme","powrprof/PowerSetActiveScheme"]
old-location: base\powersetactivescheme.htm
tech.root: power
ms.assetid: e56bc3f4-2141-4be7-8479-12f8d59971af
ms.date: 12/05/2018
ms.keywords: PowerSetActiveScheme, PowerSetActiveScheme function, base.powersetactivescheme, powersetting/PowerSetActiveScheme, powrprof/PowerSetActiveScheme
f1_keywords:
- powersetting/PowerSetActiveScheme
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- PowrProf.dll
- API-MS-Win-power-setting-l1-1-0.dll
api_name:
- PowerSetActiveScheme
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PowerSetActiveScheme function


## -description


Sets the active power scheme for the current user.


## -parameters




### -param UserRootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param SchemeGuid [in]

The identifier of the power scheme.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>
 

 

