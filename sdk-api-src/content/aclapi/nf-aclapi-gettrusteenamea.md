---
UID: NF:aclapi.GetTrusteeNameA
title: GetTrusteeNameA function
author: windows-driver-content
description: Retrieves the trustee name from the specified TRUSTEE structure.
old-location: security\gettrusteename.htm
old-project: SecAuthZ
ms.assetid: 9d3ce528-fb28-4e2e-bf7f-7d84c697fcb6
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetTrusteeName, GetTrusteeName function [Security], GetTrusteeNameA, GetTrusteeNameW, _win32_gettrusteename, aclapi/GetTrusteeName, aclapi/GetTrusteeNameA, aclapi/GetTrusteeNameW, security.gettrusteename
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
req.unicode-ansi: GetTrusteeNameW (Unicode) and GetTrusteeNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	GetTrusteeName
-	GetTrusteeNameA
-	GetTrusteeNameW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetTrusteeNameA function


## -description


The <b>GetTrusteeName</b> function retrieves the trustee name from the specified <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -parameters




### -param pTrustee [in]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -returns



If the <b>TrusteeForm</b> member of the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure is TRUSTEE_IS_NAME, the return value is the pointer assigned to the <b>ptstrName</b> member of the structure.

If the <b>TrusteeForm</b> member is TRUSTEE_IS_SID, the return value is <b>NULL</b>. The function does not look up the name associated with a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).




## -remarks



The <b>GetTrusteeName</b> function does not allocate any memory.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

