---
UID: NF:shlobj_core.IShellFolderView.SetAutomationObject
title: IShellFolderView::SetAutomationObject (shlobj_core.h)
description: Replaces the internal automation object of the IShellView.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","SetAutomationObject method","IShellFolderView.SetAutomationObject","IShellFolderView::SetAutomationObject","SetAutomationObject","SetAutomationObject method [Windows Shell]","SetAutomationObject method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_SetAutomationObject","shell.IShellFolderView_SetAutomationObject","shlobj_core/IShellFolderView::SetAutomationObject"]
old-location: shell\IShellFolderView_SetAutomationObject.htm
tech.root: shell
ms.assetid: 742b0d93-5cdf-4498-80c2-2d33359f146f
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetAutomationObject method, IShellFolderView.SetAutomationObject, IShellFolderView::SetAutomationObject, SetAutomationObject, SetAutomationObject method [Windows Shell], SetAutomationObject method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetAutomationObject, shell.IShellFolderView_SetAutomationObject, shlobj_core/IShellFolderView::SetAutomationObject
req.header: shlobj_core.h
req.include-header: 
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
 - IShellFolderView::SetAutomationObject
 - shlobj_core/IShellFolderView::SetAutomationObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.SetAutomationObject
---

# IShellFolderView::SetAutomationObject


## -description

<p class="CCE_Message">[This method is available through Windows Vista. It might be altered or unavailable in subsequent versions of Windows.]

Replaces the internal automation object of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>.

## -parameters

### -param pdisp [in, optional]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>*</b>

A pointer to the new automation object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.