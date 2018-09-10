---
UID: NF:powrprof.PowerRestoreDefaultPowerSchemes
title: PowerRestoreDefaultPowerSchemes function
author: windows-sdk-content
description: Replaces the power schemes for the system with default power schemes. All current power schemes and settings are deleted and replaced with the default system power schemes.
old-location: base\powerrestoredefaultpowerschemes.htm
tech.root: power
ms.assetid: 6d0a6167-34de-439b-afb4-2536c715905c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PowerRestoreDefaultPowerSchemes, PowerRestoreDefaultPowerSchemes function, base.powerrestoredefaultpowerschemes, powrprof/PowerRestoreDefaultPowerSchemes
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
 - PowerRestoreDefaultPowerSchemes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PowerRestoreDefaultPowerSchemes function


## -description


Replaces the power schemes for the system with default power schemes. All current 
     power schemes and settings are deleted and replaced with the default system power schemes.


## -parameters






## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -remarks



The caller must be a member of the local Administrators group.



