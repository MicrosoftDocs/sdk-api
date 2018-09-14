---
UID: NF:powrprof.PowerReplaceDefaultPowerSchemes
title: PowerReplaceDefaultPowerSchemes function
author: windows-sdk-content
description: Replaces the default power schemes with the current user's power schemes.
old-location: base\powerreplacedefaultpowerschemes.htm
tech.root: power
ms.assetid: 0d028ed9-3505-4f08-b064-14cbc8172ce0
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: PowerReplaceDefaultPowerSchemes, PowerReplaceDefaultPowerSchemes function, base.powerreplacedefaultpowerschemes, powrprof/PowerReplaceDefaultPowerSchemes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerReplaceDefaultPowerSchemes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PowerReplaceDefaultPowerSchemes function


## -description


Replaces the default power schemes with the current user's power schemes. This allows an 
    administrator to change the default power schemes for the system. Replacing the default schemes enables users to 
    use the <b>Restore Defaults</b> option in the Control Panel 
    <b>Power Options</b> application to restore customized power scheme defaults instead of the 
    original Windows power scheme defaults.


## -parameters






## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -remarks



The caller must be a member of the local Administrators group.



