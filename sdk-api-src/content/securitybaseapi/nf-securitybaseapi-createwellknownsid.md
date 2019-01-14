---
UID: NF:securitybaseapi.CreateWellKnownSid
title: CreateWellKnownSid function
author: windows-sdk-content
description: Creates a SID for predefined aliases.
old-location: security\createwellknownsid.htm
tech.root: SecAuthZ
ms.assetid: 00e75bae-fbce-41a3-a0bc-c345c36f2c84
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateWellKnownSid, CreateWellKnownSid function [Security], _win32_createwellknownsid, security.createwellknownsid, securitybaseapi/CreateWellKnownSid
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CreateWellKnownSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateWellKnownSid function


## -description


The <b>CreateWellKnownSid</b> function creates a SID for predefined aliases.


## -parameters




### -param WellKnownSidType [in]

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa379650(v=VS.85).aspx">WELL_KNOWN_SID_TYPE</a> enumeration that specifies what the SID will identify.


### -param DomainSid [in, optional]

A pointer to a SID that identifies the domain to use when creating the SID. Pass <b>NULL</b> to use the local computer.


### -param pSid [out, optional]

A pointer to memory where <b>CreateWellKnownSid</b> will store the new SID.


### -param cbSid [in, out]

A pointer to a <b>DWORD</b> that contains the number of bytes available at <i>pSid</i>. The <b>CreateWellKnownSid</b> function stores the number of bytes actually used at this location.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7eea3bd-33e0-427c-b023-07851c192eb2">EqualDomainSid</a>



<a href="https://msdn.microsoft.com/ee2ba1b4-1bef-4d79-bb18-512705e2c378">GetWindowsAccountDomainSid</a>



<a href="https://msdn.microsoft.com/1a08c70c-00fa-4c62-883d-4f17f9d7c04b">IsWellKnownSid</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379650(v=VS.85).aspx">WELL_KNOWN_SID_TYPE</a>
 

 

