---
UID: NF:powrprof.PowerIsSettingRangeDefined
title: PowerIsSettingRangeDefined function
author: windows-sdk-content
description: Queries whether the specified power setting represents a range of possible values.
old-location: base\powerissettingrangedefined.htm
old-project: Power
ms.assetid: 7babaf7b-ecb3-4b29-917e-2ed63bad4a38
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: PowerIsSettingRangeDefined, PowerIsSettingRangeDefined function, base.powerissettingrangedefined, powrprof/PowerIsSettingRangeDefined
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Powrprof.dll
api_name:
-	PowerIsSettingRangeDefined
product: Windows
targetos: Windows
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PowerIsSettingRangeDefined function


## -description


Queries whether the specified power setting represents a range of possible values.


## -parameters




### -param OPTIONAL

TBD




#### - SettingGuid [in, optional]

The identifier of the power setting to query.


#### - SubKeyGuid [in, optional]

The identifier of the subkey to search.


## -returns



TRUE if the registry key specified by <i>SubKeyGuid</i> represents a single power setting. 

If the registry key specified by <i>SubKeyGuid</i>  represents a range, this function returns FALSE.



