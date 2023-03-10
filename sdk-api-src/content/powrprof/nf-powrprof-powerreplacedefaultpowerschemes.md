---
UID: NF:powrprof.PowerReplaceDefaultPowerSchemes
title: PowerReplaceDefaultPowerSchemes function (powrprof.h)
description: Replaces the default power schemes with the current user's power schemes.
helpviewer_keywords: ["PowerReplaceDefaultPowerSchemes","PowerReplaceDefaultPowerSchemes function","base.powerreplacedefaultpowerschemes","powrprof/PowerReplaceDefaultPowerSchemes"]
old-location: base\powerreplacedefaultpowerschemes.htm
tech.root: base
ms.assetid: 0d028ed9-3505-4f08-b064-14cbc8172ce0
ms.date: 12/05/2018
ms.keywords: PowerReplaceDefaultPowerSchemes, PowerReplaceDefaultPowerSchemes function, base.powerreplacedefaultpowerschemes, powrprof/PowerReplaceDefaultPowerSchemes
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
 - PowerReplaceDefaultPowerSchemes
 - powrprof/PowerReplaceDefaultPowerSchemes
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
 - PowerReplaceDefaultPowerSchemes
---

# PowerReplaceDefaultPowerSchemes function


## -description

Replaces the default power schemes with the current user's power schemes. This allows an 
    administrator to change the default power schemes for the system. Replacing the default schemes enables users to 
    use the <b>Restore Defaults</b> option in the Control Panel 
    <b>Power Options</b> application to restore customized power scheme defaults instead of the 
    original Windows power scheme defaults.



## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

## -remarks

The caller must be a member of the local Administrators group.

