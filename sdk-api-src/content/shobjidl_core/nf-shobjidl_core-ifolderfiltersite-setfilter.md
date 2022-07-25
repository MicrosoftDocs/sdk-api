---
UID: NF:shobjidl_core.IFolderFilterSite.SetFilter
title: IFolderFilterSite::SetFilter (shobjidl_core.h)
description: Exposed by a host to allow clients to pass the host their IUnknown interface pointers.
helpviewer_keywords: ["IFolderFilterSite interface [Windows Shell]","SetFilter method","IFolderFilterSite.SetFilter","IFolderFilterSite::SetFilter","SetFilter","SetFilter method [Windows Shell]","SetFilter method [Windows Shell]","IFolderFilterSite interface","_shell_IFolderFilterSite_SetFilter","shell.IFolderFilterSite_SetFilter","shobjidl_core/IFolderFilterSite::SetFilter"]
old-location: shell\IFolderFilterSite_SetFilter.htm
tech.root: shell
ms.assetid: 1bbcb238-9b3e-4f5c-9cb3-429d0ff918af
ms.date: 12/05/2018
ms.keywords: IFolderFilterSite interface [Windows Shell],SetFilter method, IFolderFilterSite.SetFilter, IFolderFilterSite::SetFilter, SetFilter, SetFilter method [Windows Shell], SetFilter method [Windows Shell],IFolderFilterSite interface, _shell_IFolderFilterSite_SetFilter, shell.IFolderFilterSite_SetFilter, shobjidl_core/IFolderFilterSite::SetFilter
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderFilterSite::SetFilter
 - shobjidl_core/IFolderFilterSite::SetFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderFilterSite.SetFilter
---

# IFolderFilterSite::SetFilter


## -description

Exposed by a host to allow clients to pass the host their <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointers.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the client's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. To notify the host to terminate filtering and stop calling your <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter">IFolderFilter</a> interface, set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After you get a pointer to the host's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite">IFolderFilterSite</a> interface, call this method to pass the host a pointer to your <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. The host will then use this pointer to call your <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method to request a pointer to your <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter">IFolderFilter</a> interface. If this call fails, <b>IFolderFilterSite::SetFilter</b> returns <b>E_NOINTERFACEAVAILABLE</b>. If the call is successful, the host will then call the <b>IFolderFilter</b> interface's two methods to determine how to enumerate the contents of the folder.