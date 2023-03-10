---
UID: NF:shobjidl_core.IProfferService.ProfferService
title: IProfferService::ProfferService (shobjidl_core.h)
description: Makes a service available to other objects on the same host.
helpviewer_keywords: ["IProfferService interface [Windows Shell]","ProfferService method","IProfferService.ProfferService","IProfferService::ProfferService","ProfferService","ProfferService method [Windows Shell]","ProfferService method [Windows Shell]","IProfferService interface","inet_IProfferService_ProfferService","shell.IProfferService_ProfferService","shobjidl_core/IProfferService::ProfferService"]
old-location: shell\IProfferService_ProfferService.htm
tech.root: shell
ms.assetid: ebd6003d-ac8f-4e5e-9d90-c7e5688bedaa
ms.date: 12/05/2018
ms.keywords: IProfferService interface [Windows Shell],ProfferService method, IProfferService.ProfferService, IProfferService::ProfferService, ProfferService, ProfferService method [Windows Shell], ProfferService method [Windows Shell],IProfferService interface, inet_IProfferService_ProfferService, shell.IProfferService_ProfferService, shobjidl_core/IProfferService::ProfferService
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
 - IProfferService::ProfferService
 - shobjidl_core/IProfferService::ProfferService
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
 - IProfferService.ProfferService
---

# IProfferService::ProfferService


## -description

Makes a service available to other objects on the same host.

## -parameters

### -param guidService [in]

Type: <b>REFGUID</b>

A value of type <b>GUID</b> that specifies the service being offered.

### -param psp [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a>*</b>

A pointer to an <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a> interface.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> that receives an implementation-defined value used for identification purposes. The calling application must keep track of this value for possible use in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iprofferservice-revokeservice">IProfferService::RevokeService</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice">IProfferService</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iprofferservice-revokeservice">IProfferService::RevokeService</a>



<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a>