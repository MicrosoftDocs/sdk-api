---
UID: NS:ntsecpkg._SECPKG_WOW_CLIENT_DLL
title: SECPKG_WOW_CLIENT_DLL (ntsecpkg.h)
description: Contains the path to the WOW-aware 32-bit DLL.
helpviewer_keywords: ["*PSECPKG_WOW_CLIENT_DLL","PSECPKG_WOW_CLIENT_DLL","PSECPKG_WOW_CLIENT_DLL structure pointer [Security]","SECPKG_WOW_CLIENT_DLL","SECPKG_WOW_CLIENT_DLL structure [Security]","ntsecpkg/PSECPKG_WOW_CLIENT_DLL","ntsecpkg/SECPKG_WOW_CLIENT_DLL","security.secpkg_wow_client_dll"]
old-location: security\secpkg_wow_client_dll.htm
tech.root: security
ms.assetid: AA48B271-E63F-4742-9776-6C85ED3A2BAB
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_WOW_CLIENT_DLL, PSECPKG_WOW_CLIENT_DLL, PSECPKG_WOW_CLIENT_DLL structure pointer [Security], SECPKG_WOW_CLIENT_DLL, SECPKG_WOW_CLIENT_DLL structure [Security], ntsecpkg/PSECPKG_WOW_CLIENT_DLL, ntsecpkg/SECPKG_WOW_CLIENT_DLL, security.secpkg_wow_client_dll'
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SECPKG_WOW_CLIENT_DLL, *PSECPKG_WOW_CLIENT_DLL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_WOW_CLIENT_DLL
 - ntsecpkg/_SECPKG_WOW_CLIENT_DLL
 - PSECPKG_WOW_CLIENT_DLL
 - ntsecpkg/PSECPKG_WOW_CLIENT_DLL
 - SECPKG_WOW_CLIENT_DLL
 - ntsecpkg/SECPKG_WOW_CLIENT_DLL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_WOW_CLIENT_DLL
---

# SECPKG_WOW_CLIENT_DLL structure


## -description

The <b>SECPKG_WOW_CLIENT_DLL</b> structure contains the path to the WOW-aware 32-bit DLL.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field WowClientDllPath

A <a href="/windows/desktop/api/sspi/ns-sspi-security_string">SECURITY_STRING</a> that contain the path to the WOW-aware client 32-bit library.