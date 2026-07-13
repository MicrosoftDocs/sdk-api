---
UID: NF:workspaceruntime.IWorkspace3.GetClaimsToken2
title: IWorkspace3::GetClaimsToken2 (workspaceruntime.h)
description: Retrieves a claims token.
helpviewer_keywords: ["GetClaimsToken2","GetClaimsToken2 method [Remote Desktop Services]","GetClaimsToken2 method [Remote Desktop Services]","IWorkspace3 interface","IWorkspace3 interface [Remote Desktop Services]","GetClaimsToken2 method","IWorkspace3.GetClaimsToken2","IWorkspace3::GetClaimsToken2","termserv.iworkspace3_getclaimstoken2","workspaceruntime/IWorkspace3::GetClaimsToken2"]
old-location: termserv\iworkspace3_getclaimstoken2.htm
tech.root: TermServ
ms.assetid: d615b999-0713-4d16-a89b-b5b208a76124
ms.date: 12/05/2018
ms.keywords: GetClaimsToken2, GetClaimsToken2 method [Remote Desktop Services], GetClaimsToken2 method [Remote Desktop Services],IWorkspace3 interface, IWorkspace3 interface [Remote Desktop Services],GetClaimsToken2 method, IWorkspace3.GetClaimsToken2, IWorkspace3::GetClaimsToken2, termserv.iworkspace3_getclaimstoken2, workspaceruntime/IWorkspace3::GetClaimsToken2
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
 - IWorkspace3::GetClaimsToken2
 - workspaceruntime/IWorkspace3::GetClaimsToken2
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
 - IWorkspace3.GetClaimsToken2
---

# IWorkspace3::GetClaimsToken2


## -description

Retrieves a claims token.

## -parameters

### -param bstrClaimsHint [in]

String containing the claims hint.

### -param bstrUserHint [in]

String containing the user hint.

### -param claimCookie [in]

The claim cookie.

### -param hwndCredUiParent [in]

Handle of the parent UI element the request came from.

### -param rectCredUiParent [in]

Pointer to a RECT structure that contains the X and Y coordinates of the parent UI.

### -param pbstrAccessToken [out, retval]

On success, return a pointer to a string containing the access token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3">IWorkspace3</a>