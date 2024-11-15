---
UID: NF:shobjidl_core.IPreviewHandler.Unload
title: IPreviewHandler::Unload (shobjidl_core.h)
description: Directs the preview handler to cease rendering a preview and to release all resources that have been allocated based on the item passed in during the initialization.
helpviewer_keywords: ["IPreviewHandler interface [Windows Shell]","Unload method","IPreviewHandler.Unload","IPreviewHandler::Unload","Unload","Unload method [Windows Shell]","Unload method [Windows Shell]","IPreviewHandler interface","_shell_IPreviewHandler_Unload","shell.IPreviewHandler_Unload","shobjidl_core/IPreviewHandler::Unload"]
old-location: shell\IPreviewHandler_Unload.htm
tech.root: shell
ms.assetid: cefa9888-66cf-48a1-a6cd-49e273076d39
ms.date: 12/05/2018
ms.keywords: IPreviewHandler interface [Windows Shell],Unload method, IPreviewHandler.Unload, IPreviewHandler::Unload, Unload, Unload method [Windows Shell], Unload method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_Unload, shell.IPreviewHandler_Unload, shobjidl_core/IPreviewHandler::Unload
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
 - IPreviewHandler::Unload
 - shobjidl_core/IPreviewHandler::Unload
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
 - IPreviewHandler.Unload
---

# IPreviewHandler::Unload


## -description

Directs the preview handler to cease rendering a preview and to release all resources that have been allocated based on the item passed in during the initialization.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When called, the preview window will be destroyed.

This method should be called only after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize">IInitializeWithItem::Initialize</a>, <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithstream-initialize">IInitializeWithStream::Initialize</a>, or <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithfile-initialize">IInitializeWithFile::Initialize</a> has been called. All resources associated with this initialization will be released. Prior to calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview">IPreviewHandler::DoPreview</a>, this preview handler will be re-initialized with a call to one of the initialization interfaces and a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow">IPreviewHandler::SetWindow</a>.
