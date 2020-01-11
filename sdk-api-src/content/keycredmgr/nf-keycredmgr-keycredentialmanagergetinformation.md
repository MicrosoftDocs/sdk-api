---
UID: NF:keycredmgr.KeyCredentialManagerGetInformation
title: KeyCredentialManagerGetInformation function (keycredmgr.h)
description: API to get a unique identifier of the users enrollment.
old-location: security\keycredentialmanagergetinformation.htm
tech.root: SecAuthN
ms.assetid: 21664FAC-F380-4D32-A3A3-5F9326F5C79E
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerGetInformation, KeyCredentialManagerGetInformation function [Security], keycredmgr/KeyCredentialManagerGetInformation, security.keycredentialmanagergetinformation
f1_keywords:
- keycredmgr/KeyCredentialManagerGetInformation
dev_langs:
- c++
req.header: keycredmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Keycredmgr.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- keycredmgr.lib
- keycredmgr.dll
api_name:
- KeyCredentialManagerGetInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# KeyCredentialManagerGetInformation function


## -description


API to get a unique identifier of the users enrollment.


## -parameters




### -param keyCredentialManagerInfo [out]

Pointer to a pointer variable that receives a <a href="https://msdn.microsoft.com/en-us/library/Mt830289(v=VS.85).aspx">KeyCredentialManagerInfo</a> data structure.  The caller must free this pointer, when it is no longer required, by using the <a href="https://msdn.microsoft.com/en-us/library/Mt830286(v=VS.85).aspx">KeyCredentialManagerFreeInformation</a> function. 


## -returns



Returns an HRESULT.



