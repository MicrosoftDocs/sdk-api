---
UID: NF:shobjidl_core.IExplorerCommandProvider.GetCommands
title: IExplorerCommandProvider::GetCommands (shobjidl_core.h)
author: windows-sdk-content
description: Gets a specified Explorer command enumerator instance.
old-location: shell\IExplorerCommandProvider_GetCommands.htm
tech.root: shell
ms.assetid: df300219-e717-4f79-8996-62726092c3c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCommands, GetCommands method [Windows Shell], GetCommands method [Windows Shell],IExplorerCommandProvider interface, IExplorerCommandProvider interface [Windows Shell],GetCommands method, IExplorerCommandProvider.GetCommands, IExplorerCommandProvider::GetCommands, _shell_IExplorerCommandProvider_GetCommands, shell.IExplorerCommandProvider_GetCommands, shobjidl_core/IExplorerCommandProvider::GetCommands
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IExplorerCommandProvider.GetCommands"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerCommandProvider.GetCommands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerCommandProvider::GetCommands


## -description


Gets a specified Explorer command enumerator instance.


## -parameters




### -param punkSite

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an interface used to set a site.


### -param riid

Type: <b>REFIID</b>

A reference to the IID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid. This will typically be <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand">IEnumExplorerCommand</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



