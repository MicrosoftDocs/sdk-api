---
UID: NF:shobjidl_core.IPreviewHandlerFrame.GetWindowContext
title: IPreviewHandlerFrame::GetWindowContext (shobjidl_core.h)
description: Gets a list of the keyboard shortcuts for the preview host.
helpviewer_keywords: ["GetWindowContext","GetWindowContext method [Windows Shell]","GetWindowContext method [Windows Shell]","IPreviewHandlerFrame interface","IPreviewHandlerFrame interface [Windows Shell]","GetWindowContext method","IPreviewHandlerFrame.GetWindowContext","IPreviewHandlerFrame::GetWindowContext","_shell_IPreviewHandlerFrame_GetWindowContext","shell.IPreviewHandlerFrame_GetWindowContext","shobjidl_core/IPreviewHandlerFrame::GetWindowContext"]
old-location: shell\IPreviewHandlerFrame_GetWindowContext.htm
tech.root: shell
ms.assetid: 953b7571-0da1-4e31-bb6f-1761f8103c6e
ms.date: 12/05/2018
ms.keywords: GetWindowContext, GetWindowContext method [Windows Shell], GetWindowContext method [Windows Shell],IPreviewHandlerFrame interface, IPreviewHandlerFrame interface [Windows Shell],GetWindowContext method, IPreviewHandlerFrame.GetWindowContext, IPreviewHandlerFrame::GetWindowContext, _shell_IPreviewHandlerFrame_GetWindowContext, shell.IPreviewHandlerFrame_GetWindowContext, shobjidl_core/IPreviewHandlerFrame::GetWindowContext
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
f1_keywords:
 - IPreviewHandlerFrame::GetWindowContext
 - shobjidl_core/IPreviewHandlerFrame::GetWindowContext
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
 - IPreviewHandlerFrame.GetWindowContext
---

# IPreviewHandlerFrame::GetWindowContext


## -description

Gets a list of the keyboard shortcuts for the preview host.

## -parameters

### -param pinfo [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo">PREVIEWHANDLERFRAMEINFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo">PREVIEWHANDLERFRAMEINFO</a> structure that receives accelerator table information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An accelerator table is a list of keyboard shortcuts and the commands that the host should execute. As an optimization, the preview handler can then look at the keystrokes it receives, check them against the accelerator table to see if the host is interested in them, and forward them on if appropriate, ignoring the commands in the structure. The accelerator table returned from <b>IPreviewHandlerFrame::GetWindowContext</b>, contains only keystrokes and does not contain valid command entries. Preview handlers can also skip this optimization and simply call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator">IPreviewHandlerFrame::TranslateAccelerator</a> for every keystroke. When the preview handler is destroyed, the accelerator table must be freed using the <a href="/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a> function.

This method should be called at the point when the preview handler has called <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">SetSite</a> and the results have been cached for later use by the preview handler. This method cannot be called by preview handlers running in low-integrity mode.  Those preview handlers must always call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator">IPreviewHandlerFrame::TranslateAccelerator</a> for every keystroke.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe">IPreviewHandlerFrame</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator">IPreviewHandlerFrame::TranslateAccelerator</a>