---
UID: NN:shobjidl_core.IFileDialogCustomize
title: IFileDialogCustomize (shobjidl_core.h)
description: Exposes methods that allow an application to add controls to a common file dialog.
helpviewer_keywords: ["IFileDialogCustomize","IFileDialogCustomize interface [Windows Shell]","IFileDialogCustomize interface [Windows Shell]","described","shell.IFileDialogCustomize","shell_IFileDialogCustomize","shobjidl_core/IFileDialogCustomize"]
old-location: shell\IFileDialogCustomize.htm
tech.root: shell
ms.assetid: f1c29688-3538-40ff-a1da-6211cc5dded7
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize, IFileDialogCustomize interface [Windows Shell], IFileDialogCustomize interface [Windows Shell],described, shell.IFileDialogCustomize, shell_IFileDialogCustomize, shobjidl_core/IFileDialogCustomize
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
 - IFileDialogCustomize
 - shobjidl_core/IFileDialogCustomize
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
 - IFileDialogCustomize
---

# IFileDialogCustomize interface


## -description

Exposes methods that allow an application to add controls to a common file dialog.

## -inheritance

The <b>IFileDialogCustomize</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileDialogCustomize</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-ifiledialogcontrolevents">IFileDialogControlEvents</a> is implemented
by the common file open dialog (CLSID_FileOpenDialog) and
file save dialog (CLSID_FileSaveDialog).

Controls are added to the dialog before the dialog is shown. Their layout is implied by the order in which they are added. Once the dialog is shown, controls cannot be added or removed, but the existing controls can be hidden or disabled at any time. Their labels can also be changed at any time.

Container controls are controls that can have items added to them. Container controls include combo boxes, menus, the drop-down list attached to the <b>Open</b> button, and any option button groups. The order that items appear in a container is the order in which they were added. There is no facility for reordering them. IDs are scoped to the parent control. Container controls, with the exception of menus, have a selected item.

Items with a container control cannot be changed after they have been created, except for their enabled and visible states. However, they can be added and removed at any time. For example, if you needed to change the text of a menu, you would have to remove the current menu and add another with the correct text.
