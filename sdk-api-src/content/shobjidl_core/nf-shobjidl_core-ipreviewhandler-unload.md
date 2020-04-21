---
UID: NF:shobjidl_core.IPreviewHandler.Unload
title: IPreviewHandler::Unload (shobjidl_core.h)
description: Directs the preview handler to cease rendering a preview and to release all resources that have been allocated based on the item passed in during the initialization.helpviewer_keywords: ["IPreviewHandler interface [Windows Shell]","Unload method","IPreviewHandler.Unload","IPreviewHandler::Unload","Unload","Unload method [Windows Shell]","Unload method [Windows Shell]","IPreviewHandler interface","_shell_IPreviewHandler_Unload","shell.IPreviewHandler_Unload","shobjidl_core/IPreviewHandler::Unload"]
old-location: shell\IPreviewHandler_Unload.htm
tech.root: shell
ms.assetid: cefa9888-66cf-48a1-a6cd-49e273076d39
ms.date: 12/05/2018
ms.keywords: IPreviewHandler interface [Windows Shell],Unload method, IPreviewHandler.Unload, IPreviewHandler::Unload, Unload, Unload method [Windows Shell], Unload method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_Unload, shell.IPreviewHandler_Unload, shobjidl_core/IPreviewHandler::Unload
f1_keywords:
- shobjidl_core/IPreviewHandler.Unload
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IPreviewHandler.Unload
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
---

# IPreviewHandler::Unload


## -description


Directs the preview handler to cease rendering a preview and to release all resources that have been allocated based on the item passed in during the initialization.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When called, the preview window will be destroyed.

This method should be called only after <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize">Initialize</a>, <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-iinitializewithstream-initialize">Initialize</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-iinitializewithfile-initialize">Initialize</a> has been called. All resources associated with this initialization will be released. Prior to calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview">IPreviewHandler::DoPreview</a>, this preview handler will be re-initialized with a call to one of the initialization interfaces and a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow">IPreviewHandler::SetWindow</a>.



