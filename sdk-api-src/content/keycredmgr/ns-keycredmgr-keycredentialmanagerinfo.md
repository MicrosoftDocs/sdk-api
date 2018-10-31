---
UID: NS:keycredmgr.KeyCredentialManagerInfo
title: KeyCredentialManagerInfo
author: windows-sdk-content
description: Data structure returned from KeyCredentialManagerGetInformation.
old-location: security\keycredentialmanagerinfo.htm
tech.root: secauthn
ms.assetid: BF573834-FA5A-4ADE-9E19-389B1A15A1F8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: KeyCredentialManagerInfo, KeyCredentialManagerInfo structure [Security], PKeyCredentialManagerInfo, PKeyCredentialManagerInfo structure pointer [Security], keycredmgr/KeyCredentialManagerInfo, keycredmgr/PKeyCredentialManagerInfo, security.keycredentialmanagerinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: KeyCredentialManagerInfo
req.redist: 
---

# KeyCredentialManagerInfo structure


## -description


Data structure returned from <a href="security.keycredentialmanagergetinformation">KeyCredentialManagerGetInformation</a>.


## -struct-fields




### -field containerId

Unique identifier of the users WHFB container. Only one container per Windows user profile.

