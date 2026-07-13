---
UID: NF:workspaceruntime.IWorkspace3.SetClaimsToken
title: IWorkspace3::SetClaimsToken (workspaceruntime.h)
description: Sets the claims token.
helpviewer_keywords: ["IWorkspace3 interface [Remote Desktop Services]","SetClaimsToken method","IWorkspace3.SetClaimsToken","IWorkspace3::SetClaimsToken","SetClaimsToken","SetClaimsToken method [Remote Desktop Services]","SetClaimsToken method [Remote Desktop Services]","IWorkspace3 interface","termserv.iworkspace3_setclaimstoken","workspaceruntime/IWorkspace3::SetClaimsToken"]
old-location: termserv\iworkspace3_setclaimstoken.htm
tech.root: TermServ
ms.assetid: 221b0e8f-b43a-4942-9e70-152daf5b1ef0
ms.date: 12/05/2018
ms.keywords: IWorkspace3 interface [Remote Desktop Services],SetClaimsToken method, IWorkspace3.SetClaimsToken, IWorkspace3::SetClaimsToken, SetClaimsToken, SetClaimsToken method [Remote Desktop Services], SetClaimsToken method [Remote Desktop Services],IWorkspace3 interface, termserv.iworkspace3_setclaimstoken, workspaceruntime/IWorkspace3::SetClaimsToken
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspace3::SetClaimsToken
 - workspaceruntime/IWorkspace3::SetClaimsToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - workspaceruntime.h
api_name:
 - IWorkspace3.SetClaimsToken
---

# IWorkspace3::SetClaimsToken


## -description

Sets the claims token.

## -parameters

### -param bstrAccessToken [in]

A string containing the access token.

### -param ullAccessTokenExpiration [in]

The time, in milliseconds, until the access token expires.

### -param bstrRefreshToken [in]

A string containing the refresh token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3">IWorkspace3</a>