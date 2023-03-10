---
UID: NN:shobjidl_core.IApplicationDocumentLists
title: IApplicationDocumentLists (shobjidl_core.h)
description: Exposes methods that allow an application to retrieve the contents of the Recent or Frequent categories in a Jump List.
helpviewer_keywords: ["IApplicationDocumentLists","IApplicationDocumentLists interface [Windows Shell]","IApplicationDocumentLists interface [Windows Shell]","described","_shell_IApplicationDocumentLists","shell.IApplicationDocumentLists","shobjidl_core/IApplicationDocumentLists"]
old-location: shell\IApplicationDocumentLists.htm
tech.root: shell
ms.assetid: 1912d8fd-1724-4a4b-b74a-e05db12ffead
ms.date: 12/05/2018
ms.keywords: IApplicationDocumentLists, IApplicationDocumentLists interface [Windows Shell], IApplicationDocumentLists interface [Windows Shell],described, _shell_IApplicationDocumentLists, shell.IApplicationDocumentLists, shobjidl_core/IApplicationDocumentLists
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDocumentLists
 - shobjidl_core/IApplicationDocumentLists
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
 - IApplicationDocumentLists
---

# IApplicationDocumentLists interface


## -description

Exposes methods that allow an application to retrieve the contents of the <b>Recent</b> or <b>Frequent</b> categories in a Jump List.

## -inheritance

The <b>IApplicationDocumentLists</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationDocumentLists</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_ApplicationDocumentLists. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
An application calls the methods of this interface when it wants to retrieve a Jump List's <b>Recent</b> or <b>Frequent</b> list. These lists are generated through calls to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>, either explicitly or by the system when a file is opened through Windows Explorer or the common file dialog is used to open, save, or create a file.



<b>IApplicationDocumentLists</b> is used only with the automatically generated <b>Recent</b> or <b>Frequent</b> categories. It cannot retrieve a list of items that the user has pinned to the Jump List. That list cannot be retrieved programmatically because it cannot be manipulated programmatically; it is strictly under the user's control. <b>IApplicationDocumentLists</b> also cannot access custom categories or the task list.

## -see-also

<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
