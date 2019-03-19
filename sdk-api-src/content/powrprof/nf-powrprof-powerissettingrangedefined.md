---
UID: NF:powrprof.PowerIsSettingRangeDefined
title: PowerIsSettingRangeDefined function (powrprof.h)
author: windows-sdk-content
description: Queries whether the specified power setting represents a range of possible values.
old-location: base\powerissettingrangedefined.htm
tech.root: power
ms.assetid: 7babaf7b-ecb3-4b29-917e-2ed63bad4a38
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PowerIsSettingRangeDefined, PowerIsSettingRangeDefined function, base.powerissettingrangedefined, powrprof/PowerIsSettingRangeDefined
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
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
api_name:
 - PowerIsSettingRangeDefined
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PowerIsSettingRangeDefined function


## -description


Queries whether the specified power setting represents a range of possible values.


## -parameters




### -param SubKeyGuid [in, optional]

The identifier of the subkey to search.


### -param SettingGuid [in, optional]

The identifier of the power setting to query.


## -returns



TRUE if the registry key specified by <i>SubKeyGuid</i> represents a single power setting. 

If the registry key specified by <i>SubKeyGuid</i>  represents a range, this function returns FALSE.



