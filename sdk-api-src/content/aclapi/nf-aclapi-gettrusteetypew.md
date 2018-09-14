---
UID: NF:aclapi.GetTrusteeTypeW
title: GetTrusteeTypeW function
author: windows-sdk-content
description: Retrieves the trustee type from the specified TRUSTEE structure. This value indicates whether the trustee is a user, a group, or the trustee type is unknown.
old-location: security\gettrusteetype.htm
tech.root: secauthz
ms.assetid: 19777929-43cf-45ea-8283-e42bf9ce8d7a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetTrusteeType, GetTrusteeType function [Security], GetTrusteeTypeA, GetTrusteeTypeW, _win32_gettrusteetype, aclapi/GetTrusteeType, aclapi/GetTrusteeTypeA, aclapi/GetTrusteeTypeW, security.gettrusteetype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTrusteeTypeW (Unicode) and GetTrusteeTypeA (ANSI)
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
api_name:
 - GetTrusteeType
 - GetTrusteeTypeA
 - GetTrusteeTypeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTrusteeTypeW function


## -description


The <b>GetTrusteeType</b> function retrieves the trustee type from the specified <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. This value indicates whether the trustee is a user, a group, or the trustee type is unknown.


## -parameters




### -param pTrustee [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -returns



The return value is one of the constants from the <a href="https://msdn.microsoft.com/6519c79d-9cee-4565-a71e-0b81a27c1185">TRUSTEE_TYPE</a> enumeration.
					




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>



<a href="https://msdn.microsoft.com/6519c79d-9cee-4565-a71e-0b81a27c1185">TRUSTEE_TYPE</a>
 

 

