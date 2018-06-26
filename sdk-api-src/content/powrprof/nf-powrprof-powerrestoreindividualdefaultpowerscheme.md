---
UID: NF:powrprof.PowerRestoreIndividualDefaultPowerScheme
title: PowerRestoreIndividualDefaultPowerScheme function
author: windows-sdk-content
description: Replaces a specific power scheme for the current user with one from the default user (stored in HKEY_USERS\.Default).
old-location: base\powerrestoreindividualdefaultpowerscheme.htm
old-project: Power
ms.assetid: f1a9cfb1-1b56-4873-994b-7fe929fdc86c
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: PowerRestoreIndividualDefaultPowerScheme, PowerRestoreIndividualDefaultPowerScheme function, base.powerrestoreindividualdefaultpowerscheme, powrprof/PowerRestoreIndividualDefaultPowerScheme
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerRestoreIndividualDefaultPowerScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: ADAM
---

# PowerRestoreIndividualDefaultPowerScheme function


## -description


Replaces a specific power scheme for the current user with one from the default user (stored in 
    <b>HKEY_USERS</b>\<b>.Default</b>)


## -parameters




### -param SchemeGuid [in]

The identifier of the power scheme.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
	     the call failed.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

