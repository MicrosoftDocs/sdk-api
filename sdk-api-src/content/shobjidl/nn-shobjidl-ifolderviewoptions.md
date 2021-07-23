---
UID: NN:shobjidl.IFolderViewOptions
title: IFolderViewOptions (shobjidl.h)
description: Exposes methods that allow control of folder view options specific to the Windows 7 and later views.
helpviewer_keywords: ["IFolderViewOptions","IFolderViewOptions interface [Windows Shell]","IFolderViewOptions interface [Windows Shell]","described","_shell_IFolderViewOptions","shell.IFolderViewOptions","shobjidl/IFolderViewOptions"]
old-location: shell\IFolderViewOptions.htm
tech.root: shell
ms.assetid: 4831e62c-45e4-435d-b926-0e140cbfb6fc
ms.date: 12/05/2018
ms.keywords: IFolderViewOptions, IFolderViewOptions interface [Windows Shell], IFolderViewOptions interface [Windows Shell],described, _shell_IFolderViewOptions, shell.IFolderViewOptions, shobjidl/IFolderViewOptions
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: ExplorerFrame.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderViewOptions
 - shobjidl/IFolderViewOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ExplorerFrame.dll
api_name:
 - IFolderViewOptions
---

# IFolderViewOptions interface


## -description

Exposes methods that allow control of folder view options specific to the Windows 7 and later views.

## -inheritance

The <b>IFolderViewOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFolderViewOptions</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows as part of CLSID_ExplorerBrowser and CLSID_ShellBrowser. Third parties do not implement this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
By default, the Windows 7 item view does not support custom positioning, custom ordering, or hyperlinks, which were supported in the Windows Vista list view. Use this interface when you require those features of the older view. If, at some later time, the item view adds support for those features, these options will automatically use the newer view rather than continuing to revert to the older view as they currently do.



Use this interface to turn off animation and scroll tip view options new to Windows 7.

Use this interface to retrieve the current view settings for all of those options.
