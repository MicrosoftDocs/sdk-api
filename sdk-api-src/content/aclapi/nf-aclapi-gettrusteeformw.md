---
UID: NF:aclapi.GetTrusteeFormW
title: GetTrusteeFormW function
author: windows-sdk-content
description: Retrieves the trustee name from the specified TRUSTEE structure. This value indicates whether the structure uses a name string or a security identifier (SID) to identify the trustee.
old-location: security\gettrusteeform.htm
tech.root: SecAuthZ
ms.assetid: e5e450b8-0b7b-4324-b453-5c020e74b1ee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTrusteeForm, GetTrusteeForm function [Security], GetTrusteeFormA, GetTrusteeFormW, _win32_gettrusteeform, aclapi/GetTrusteeForm, aclapi/GetTrusteeFormA, aclapi/GetTrusteeFormW, security.gettrusteeform
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
req.unicode-ansi: GetTrusteeFormW (Unicode) and GetTrusteeFormA (ANSI)
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
 - GetTrusteeForm
 - GetTrusteeFormA
 - GetTrusteeFormW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTrusteeFormW function


## -description


The <b>GetTrusteeForm</b> function retrieves the trustee name from the specified <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. This value indicates whether the structure uses a name string or a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to identify the trustee.


## -parameters




### -param pTrustee [in]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -returns



The return value is one of the constants from the 
<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a> enumeration.
					




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/9d3ce528-fb28-4e2e-bf7f-7d84c697fcb6">GetTrusteeName</a>



<a href="https://msdn.microsoft.com/19777929-43cf-45ea-8283-e42bf9ce8d7a">GetTrusteeType</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>



<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a>
 

 

