---
UID: NF:shobjidl.IDeskBand2.CanRenderComposited
title: IDeskBand2::CanRenderComposited (shobjidl.h)
description: Indicates the deskband's ability to be displayed as translucent.
helpviewer_keywords: ["CanRenderComposited","CanRenderComposited method [Windows Shell]","CanRenderComposited method [Windows Shell]","IDeskBand2 interface","IDeskBand2 interface [Windows Shell]","CanRenderComposited method","IDeskBand2.CanRenderComposited","IDeskBand2::CanRenderComposited","_shell_IDeskBand2_CanRenderComposited","shell.IDeskBand2_CanRenderComposited","shobjidl/IDeskBand2::CanRenderComposited"]
old-location: shell\IDeskBand2_CanRenderComposited.htm
tech.root: shell
ms.assetid: af42c03f-04aa-42b2-9be4-b3bfa0a8c47e
ms.date: 12/05/2018
ms.keywords: CanRenderComposited, CanRenderComposited method [Windows Shell], CanRenderComposited method [Windows Shell],IDeskBand2 interface, IDeskBand2 interface [Windows Shell],CanRenderComposited method, IDeskBand2.CanRenderComposited, IDeskBand2::CanRenderComposited, _shell_IDeskBand2_CanRenderComposited, shell.IDeskBand2_CanRenderComposited, shobjidl/IDeskBand2::CanRenderComposited
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IDeskBand2::CanRenderComposited
 - shobjidl/IDeskBand2::CanRenderComposited
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
 - IDeskBand2.CanRenderComposited
---

# IDeskBand2::CanRenderComposited


## -description

Indicates the deskband's ability to be displayed as translucent.
<div class="alert"><b>Important</b>  You should use <a href="/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters

### -param pfCanRenderComposited [out]

Type: <b>BOOL*</b>

When this method returns, contains a <b>BOOL</b> indicating ability.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.