---
UID: NF:shobjidl_core.IPreviewHandler.Unload
title: IPreviewHandler::Unload
author: windows-sdk-content
description: Directs the preview handler to cease rendering a preview and to release all resources that have been allocated based on the item passed in during the initialization.
old-location: shell\IPreviewHandler_Unload.htm
old-project: shell
ms.assetid: cefa9888-66cf-48a1-a6cd-49e273076d39
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IPreviewHandler interface [Windows Shell],Unload method, IPreviewHandler.Unload, IPreviewHandler::Unload, Unload, Unload method [Windows Shell], Unload method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_Unload, shell.IPreviewHandler_Unload, shobjidl_core/IPreviewHandler::Unload
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPreviewHandler.Unload
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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

This method should be called only after <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> has been called. All resources associated with this initialization will be released. Prior to calling <a href="https://msdn.microsoft.com/f6bad84f-9089-4905-ad4d-9b69ff9d11d6">IPreviewHandler::DoPreview</a>, this preview handler will be re-initialized with a call to one of the initialization interfaces and a call to <a href="https://msdn.microsoft.com/a323811a-8244-40a0-a6b2-68572639be5f">IPreviewHandler::SetWindow</a>.



