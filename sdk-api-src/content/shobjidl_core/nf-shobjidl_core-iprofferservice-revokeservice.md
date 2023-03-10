---
UID: NF:shobjidl_core.IProfferService.RevokeService
title: IProfferService::RevokeService (shobjidl_core.h)
description: Makes a service unavailable that had previously been available to other objects through IProfferService::ProfferService.
helpviewer_keywords: ["IProfferService interface [Windows Shell]","RevokeService method","IProfferService.RevokeService","IProfferService::RevokeService","RevokeService","RevokeService method [Windows Shell]","RevokeService method [Windows Shell]","IProfferService interface","inet_IProfferService_RevokeService","shell.IProfferService_RevokeService","shobjidl_core/IProfferService::RevokeService"]
old-location: shell\IProfferService_RevokeService.htm
tech.root: shell
ms.assetid: 90868bbb-6fcd-4de1-a853-524542b74701
ms.date: 12/05/2018
ms.keywords: IProfferService interface [Windows Shell],RevokeService method, IProfferService.RevokeService, IProfferService::RevokeService, RevokeService, RevokeService method [Windows Shell], RevokeService method [Windows Shell],IProfferService interface, inet_IProfferService_RevokeService, shell.IProfferService_RevokeService, shobjidl_core/IProfferService::RevokeService
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProfferService::RevokeService
 - shobjidl_core/IProfferService::RevokeService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IProfferService.RevokeService
---

# IProfferService::RevokeService


## -description

Makes a service unavailable that had previously been available to other objects through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iprofferservice-profferservice">IProfferService::ProfferService</a>.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies an implementation-defined value used for identification purposes. The calling application receives this value from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iprofferservice-profferservice">IProfferService::ProfferService</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice">IProfferService</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iprofferservice-profferservice">IProfferService::ProfferService</a>