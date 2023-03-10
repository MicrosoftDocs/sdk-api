---
UID: NN:shobjidl_core.IEnumExplorerCommand
title: IEnumExplorerCommand (shobjidl_core.h)
description: Provided by an IExplorerCommandProvider. This interface contains the enumeration of commands to be put into the command bar.
helpviewer_keywords: ["IEnumExplorerCommand","IEnumExplorerCommand interface [Windows Shell]","IEnumExplorerCommand interface [Windows Shell]","described","_shell_IEnumExplorerCommand","shell.IEnumExplorerCommand","shobjidl_core/IEnumExplorerCommand"]
old-location: shell\IEnumExplorerCommand.htm
tech.root: shell
ms.assetid: c9a21e84-dd95-413a-b9db-e02008185bef
ms.date: 12/05/2018
ms.keywords: IEnumExplorerCommand, IEnumExplorerCommand interface [Windows Shell], IEnumExplorerCommand interface [Windows Shell],described, _shell_IEnumExplorerCommand, shell.IEnumExplorerCommand, shobjidl_core/IEnumExplorerCommand
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
 - IEnumExplorerCommand
 - shobjidl_core/IEnumExplorerCommand
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
 - IEnumExplorerCommand
---

# IEnumExplorerCommand interface


## -description

Provided by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider">IExplorerCommandProvider</a>. This interface contains the enumeration of commands to be put into the command bar.

## -inheritance

The <b>IEnumExplorerCommand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumExplorerCommand</b> also has these types of members:

## -remarks

None of the methods of this interface should talk to network resources. They are called on the UI thread; communicating with network resources would cause the UI to stop responding.
