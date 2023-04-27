---
UID: NN:shobjidl_core.IExplorerCommand
title: IExplorerCommand (shobjidl_core.h)
description: Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.
helpviewer_keywords: ["IExplorerCommand","IExplorerCommand interface [Windows Shell]","IExplorerCommand interface [Windows Shell]","described","_shell_IExplorerCommand","shell.IExplorerCommand","shobjidl_core/IExplorerCommand"]
old-location: shell\IExplorerCommand.htm
tech.root: shell
ms.assetid: 61e94e50-9e12-4a2c-a6c7-64a9181f80b8
ms.date: 12/05/2018
ms.keywords: IExplorerCommand, IExplorerCommand interface [Windows Shell], IExplorerCommand interface [Windows Shell],described, _shell_IExplorerCommand, shell.IExplorerCommand, shobjidl_core/IExplorerCommand
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExplorerCommand
 - shobjidl_core/IExplorerCommand
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
 - IExplorerCommand
---

# IExplorerCommand interface


## -description

Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.

## -inheritance

The <b>IExplorerCommand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerCommand</b> also has these types of members:

## -remarks

None of the methods of this interface should communicate with network resources. These methods are called on the UI thread, so communication with network resources could cause the UI to stop responding.

Note: Windows 11 refines the behavior of the contextual file operations in the right-click context menu of File Explorer and the Share dialog. Please see  <a href="/windows/apps/get-started/make-apps-great-for-windows">Top 11 things you can do to make your app great on Windows 11 </a>
