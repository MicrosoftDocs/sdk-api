---
UID: NF:securitybaseapi.IsWellKnownSid
title: IsWellKnownSid function
author: windows-sdk-content
description: Compares a SID to a well-known SID and returns TRUE if they match.
old-location: security\iswellknownsid.htm
tech.root: SecAuthZ
ms.assetid: 1a08c70c-00fa-4c62-883d-4f17f9d7c04b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IsWellKnownSid, IsWellKnownSid function [Security], _win32_iswellknownsid, security.iswellknownsid, securitybaseapi/IsWellKnownSid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - IsWellKnownSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsWellKnownSid
: 
---

# IsWellKnownSid function


## -description


The <b>IsWellKnownSid</b> function compares a SID to a well-known SID and returns <b>TRUE</b> if they match.


## -parameters




### -param pSid [in]

A pointer to the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> to test.


### -param WellKnownSidType [in]

Member of the 
<a href="https://msdn.microsoft.com/6f1fa59e-17c0-412b-937b-ddf746ed68bd">WELL_KNOWN_SID_TYPE</a> enumeration to compare with the SID at <i>pSid</i>.


## -returns



Returns <b>TRUE</b> if the SID at <i>pSid</i> matches the well-known SID indicated by <i>WellKnownSidType</i>.

Otherwise, returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/6f1fa59e-17c0-412b-937b-ddf746ed68bd">WELL_KNOWN_SID_TYPE</a>
 

 

