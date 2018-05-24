---
UID: NF:ras.RasFreeEapUserIdentityA
title: RasFreeEapUserIdentityA function
author: windows-driver-content
description: Use the RasFreeEapUserIdentity function to free the memory buffer returned by RasGetEapUserIdentity.
old-location: rras\rasfreeeapuseridentity.htm
old-project: RRAS
ms.assetid: 84102fdc-b44a-415e-b67e-58c82e662a23
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: RasFreeEapUserIdentity, RasFreeEapUserIdentity function [RAS], RasFreeEapUserIdentityA, RasFreeEapUserIdentityW, _ras_rasfreeeapuseridentity, ras/RasFreeEapUserIdentity, ras/RasFreeEapUserIdentityA, ras/RasFreeEapUserIdentityW, rras.rasfreeeapuseridentity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasFreeEapUserIdentityW (Unicode) and RasFreeEapUserIdentityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rasapi32.dll
api_name:
-	RasFreeEapUserIdentity
-	RasFreeEapUserIdentityA
-	RasFreeEapUserIdentityW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RasFreeEapUserIdentityA function


## -description


Use the 
<b>RasFreeEapUserIdentity</b> function to free the memory buffer returned by 
<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a>.


## -parameters




### -param pRasEapUserIdentity [in]

Pointer to the 
<a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a> structure returned by the 
<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a> function. 
<b>RasFreeEapUserIdentity</b> frees the memory occupied by this structure.


## -returns



This function does not return a value.




## -remarks



<b>RasFreeEapUserIdentity</b> can be called with the <i>pRasEapUserIdentity</i> parameter equal to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a>



<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a>
 

 

