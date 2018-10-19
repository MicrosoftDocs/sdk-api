---
UID: NF:securitybaseapi.GetLengthSid
title: GetLengthSid function
author: windows-sdk-content
description: Returns the length, in bytes, of a valid security identifier (SID).
old-location: security\getlengthsid.htm
tech.root: SecAuthZ
ms.assetid: 0acaa804-494c-4d69-b1f7-8d167b494761
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetLengthSid, GetLengthSid function [Security], _win32_getlengthsid, security.getlengthsid, securitybaseapi/GetLengthSid
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - GetLengthSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLengthSid function


## -description


The <b>GetLengthSid</b> function returns the length, in bytes, of a valid <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


## -parameters




### -param pSid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure whose length is returned. The structure is assumed to be valid.


## -returns



If the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure is valid, the return value is the length, in bytes, of the <b>SID</b> structure.

If the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure is not valid, the return value is undefined. Before calling <b>GetLengthSid</b>, pass the SID to the 
<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a> function to verify that the SID is valid.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/a481fb4f-20bd-4f44-a3d5-d8b8d6228339">GetSidLengthRequired</a>



<a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

