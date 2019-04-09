---
UID: NF:powrprof.PowerDeleteScheme
title: PowerDeleteScheme function (powrprof.h)
author: windows-sdk-content
description: Deletes the specified power scheme from the database.
old-location: base\powerdeletescheme.htm
tech.root: power
ms.assetid: 5f9969a1-e598-4ca8-a5b8-f8bb3410223d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PowerDeleteScheme, PowerDeleteScheme function, base.powerdeletescheme, powrprof/PowerDeleteScheme
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
 - PowerDeleteScheme
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PowerDeleteScheme function


## -description


Deletes the specified power scheme from the database.


## -parameters




### -param RootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param SchemeGuid [in]

The identifier of the power scheme.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

