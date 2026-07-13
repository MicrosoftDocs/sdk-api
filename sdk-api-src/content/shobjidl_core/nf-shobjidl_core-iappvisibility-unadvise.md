---
UID: NF:shobjidl_core.IAppVisibility.Unadvise
title: IAppVisibility::Unadvise (shobjidl_core.h)
description: Cancels a connection that was previously established by using Advise.
helpviewer_keywords: ["IAppVisibility interface [Windows Shell]","Unadvise method","IAppVisibility.Unadvise","IAppVisibility::Unadvise","Unadvise","Unadvise method [Windows Shell]","Unadvise method [Windows Shell]","IAppVisibility interface","shell.IAppVisibility_Unadvise","shobjidl_core/IAppVisibility::Unadvise"]
old-location: shell\IAppVisibility_Unadvise.htm
tech.root: shell
ms.assetid: D670F1E7-5E0B-498E-8F27-DF2A3A387862
ms.date: 12/05/2018
ms.keywords: IAppVisibility interface [Windows Shell],Unadvise method, IAppVisibility.Unadvise, IAppVisibility::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IAppVisibility interface, shell.IAppVisibility_Unadvise, shobjidl_core/IAppVisibility::Unadvise
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppVisibility::Unadvise
 - shobjidl_core/IAppVisibility::Unadvise
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
 - IAppVisibility.Unadvise
---

# IAppVisibility::Unadvise


## -description

Cancels a connection that was previously established by using <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-advise">Advise</a>.

## -parameters

### -param dwCookie [in]

A token that uniquely identifies the connection to cancel, which is provided by a previous call to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-advise">Advise</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents">IAppVisibilityEvents</a>