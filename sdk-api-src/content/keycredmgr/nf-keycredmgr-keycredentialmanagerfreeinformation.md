---
UID: NF:keycredmgr.KeyCredentialManagerFreeInformation
title: KeyCredentialManagerFreeInformation function (keycredmgr.h)
description: API to free the KeyCredentialManagerInfo pointer variable from the KeyCredentialManagerGetInformation call.
helpviewer_keywords: ["KeyCredentialManagerFreeInformation","KeyCredentialManagerFreeInformation function [Security]","keycredmgr/KeyCredentialManagerFreeInformation","security.keycredentialmanagerfreeinformation"]
old-location: security\keycredentialmanagerfreeinformation.htm
tech.root: security
ms.assetid: CE89671C-C70D-49C0-AA22-E39EEAA310D7
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerFreeInformation, KeyCredentialManagerFreeInformation function [Security], keycredmgr/KeyCredentialManagerFreeInformation, security.keycredentialmanagerfreeinformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KeyCredentialManagerFreeInformation
 - keycredmgr/KeyCredentialManagerFreeInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - keycredmgr.lib
 - keycredmgr.dll
api_name:
 - KeyCredentialManagerFreeInformation
---

# KeyCredentialManagerFreeInformation function


## -description

API to free the <a href="../keycredmgr/ns-keycredmgr-keycredentialmanagerinfo.md">KeyCredentialManagerInfo</a> pointer variable from the <a href="../keycredmgr/nf-keycredmgr-keycredentialmanagergetinformation.md">KeyCredentialManagerGetInformation</a> call.

## -parameters

### -param keyCredentialManagerInfo [in]

Pointer variable to <a href="../keycredmgr/ns-keycredmgr-keycredentialmanagerinfo.md">KeyCredentialManagerInfo</a> data structure returned by the <a href="../keycredmgr/nf-keycredmgr-keycredentialmanagergetinformation.md">KeyCredentialManagerGetInformation</a> API.

