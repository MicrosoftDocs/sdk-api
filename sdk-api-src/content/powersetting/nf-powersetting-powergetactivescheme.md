---
UID: NF:powersetting.PowerGetActiveScheme
title: PowerGetActiveScheme function
author: windows-sdk-content
description: Retrieves the active power scheme and returns a GUID that identifies the scheme.
old-location: base\powergetactivescheme.htm
old-project: power
ms.assetid: cd72562c-8987-40c1-89c7-04a95b5f1fd0
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: PowerGetActiveScheme, PowerGetActiveScheme function, base.powergetactivescheme, powersetting/PowerGetActiveScheme, powrprof/PowerGetActiveScheme
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
 - API-MS-Win-power-setting-l1-1-0.dll
api_name:
 - PowerGetActiveScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: ADAM
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
      Use the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to free this memory.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

