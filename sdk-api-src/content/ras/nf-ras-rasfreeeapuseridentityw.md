---
UID: NF:ras.RasFreeEapUserIdentityW
title: RasFreeEapUserIdentityW function (ras.h)
description: Use the RasFreeEapUserIdentity function to free the memory buffer returned by RasGetEapUserIdentity.
old-location: rras\rasfreeeapuseridentity.htm
tech.root: RRAS
ms.assetid: 84102fdc-b44a-415e-b67e-58c82e662a23
ms.date: 12/05/2018
ms.keywords: RasFreeEapUserIdentity, RasFreeEapUserIdentity function [RAS], RasFreeEapUserIdentityA, RasFreeEapUserIdentityW, _ras_rasfreeeapuseridentity, ras/RasFreeEapUserIdentity, ras/RasFreeEapUserIdentityA, ras/RasFreeEapUserIdentityW, rras.rasfreeeapuseridentity
f1_keywords:
- ras/RasFreeEapUserIdentity
dev_langs:
- c++
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
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Rasapi32.dll
api_name:
- RasFreeEapUserIdentity
- RasFreeEapUserIdentityA
- RasFreeEapUserIdentityW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasFreeEapUserIdentityW function


## -description


Use the 
<b>RasFreeEapUserIdentity</b> function to free the memory buffer returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a>.


## -parameters




### -param pRasEapUserIdentity [in]

Pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a> structure returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a> function. 
<b>RasFreeEapUserIdentity</b> frees the memory occupied by this structure.


## -remarks



<b>RasFreeEapUserIdentity</b> can be called with the <i>pRasEapUserIdentity</i> parameter equal to <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a>
 

 

