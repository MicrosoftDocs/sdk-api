---
UID: NF:keycredmgr.KeyCredentialManagerFreeInformation
title: KeyCredentialManagerFreeInformation function (keycredmgr.h)
author: windows-sdk-content
description: API to free the KeyCredentialManagerInfo pointer variable from the KeyCredentialManagerGetInformation call.
old-location: security\keycredentialmanagerfreeinformation.htm
tech.root: SecAuthN
ms.assetid: CE89671C-C70D-49C0-AA22-E39EEAA310D7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerFreeInformation, KeyCredentialManagerFreeInformation function [Security], keycredmgr/KeyCredentialManagerFreeInformation, security.keycredentialmanagerfreeinformation
ms.topic: function
f1_keywords: 
 - "keycredmgr/KeyCredentialManagerFreeInformation"
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
 - KeyCredentialManagerFreeInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# KeyCredentialManagerFreeInformation function


## -description


API to free the <a href="https://msdn.microsoft.com/en-us/library/Mt830289(v=VS.85).aspx">KeyCredentialManagerInfo</a> pointer variable from the <a href="https://msdn.microsoft.com/en-us/library/Mt830287(v=VS.85).aspx">KeyCredentialManagerGetInformation</a> call.


## -parameters




### -param keyCredentialManagerInfo [in]

Pointer variable to <a href="https://msdn.microsoft.com/en-us/library/Mt830289(v=VS.85).aspx">KeyCredentialManagerInfo</a> data structure returned by the <a href="https://msdn.microsoft.com/en-us/library/Mt830287(v=VS.85).aspx">KeyCredentialManagerGetInformation</a> API.

