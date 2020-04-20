---
UID: NS:keycredmgr.KeyCredentialManagerInfo
title: KeyCredentialManagerInfo (keycredmgr.h)
description: Data structure returned from KeyCredentialManagerGetInformation.helpviewer_keywords: ["KeyCredentialManagerInfo","KeyCredentialManagerInfo structure [Security]","PKeyCredentialManagerInfo","PKeyCredentialManagerInfo structure pointer [Security]","keycredmgr/KeyCredentialManagerInfo","keycredmgr/PKeyCredentialManagerInfo","security.keycredentialmanagerinfo"]
old-location: security\keycredentialmanagerinfo.htm
tech.root: SecAuthN
ms.assetid: BF573834-FA5A-4ADE-9E19-389B1A15A1F8
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerInfo, KeyCredentialManagerInfo structure [Security], PKeyCredentialManagerInfo, PKeyCredentialManagerInfo structure pointer [Security], keycredmgr/KeyCredentialManagerInfo, keycredmgr/PKeyCredentialManagerInfo, security.keycredentialmanagerinfo
f1_keywords:
- keycredmgr/KeyCredentialManagerInfo
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- keycredmgr.h
api_name:
- KeyCredentialManagerInfo
targetos: Windows
req.typenames: KeyCredentialManagerInfo
req.redist: 
ms.custom: 19H1
---

# KeyCredentialManagerInfo structure


## -description


Data structure returned from <a href="https://msdn.microsoft.com/en-us/library/Mt830287(v=VS.85).aspx">KeyCredentialManagerGetInformation</a>.


## -struct-fields




### -field containerId

Unique identifier of the users WHFB container. Only one container per Windows user profile.

