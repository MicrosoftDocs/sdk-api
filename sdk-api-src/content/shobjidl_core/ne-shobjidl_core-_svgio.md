---
UID: NE:shobjidl_core._SVGIO
title: "_SVGIO"
author: windows-sdk-content
description: Used with the IFolderView::Items, IFolderView::ItemCount, and IShellView::GetItemObject methods to restrict or control the items in their collections.
old-location: shell\SVGIO.htm
old-project: shell
ms.assetid: 06ed616b-8121-4ea0-bd05-632888d0f376
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SVGIO_ALLVIEW, SVGIO_BACKGROUND, SVGIO_CHECKED, SVGIO_FLAG_VIEWORDER, SVGIO_SELECTION, SVGIO_TYPE_MASK, _SVGIO, _SVGIO enumeration [Windows Shell], _shell_SVGIO, shell.SVGIO, shobjidl_core/SVGIO_ALLVIEW, shobjidl_core/SVGIO_BACKGROUND, shobjidl_core/SVGIO_CHECKED, shobjidl_core/SVGIO_FLAG_VIEWORDER, shobjidl_core/SVGIO_SELECTION, shobjidl_core/SVGIO_TYPE_MASK, shobjidl_core/_SVGIO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
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
tech.root: 
req.typenames: "_SVGIO"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - _SVGIO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SVGIO enumeration


## -description


Used with the <a href="https://msdn.microsoft.com/f93e2d30-7b50-48e8-a3e7-6fa29abb8a32">IFolderView::Items</a>, <a href="https://msdn.microsoft.com/dadf91c5-7d27-4b1b-875b-6f0615440f47">IFolderView::ItemCount</a>, and <a href="https://msdn.microsoft.com/249ce8cc-6820-4f0a-a83a-2035e88d0d9c">IShellView::GetItemObject</a> methods to restrict or control the items in their collections.


## -enum-fields




### -field SVGIO_BACKGROUND

0x00000000. Refers to the background of the view. It is used with IID_IContextMenu to get a shortcut menu for the view background and with IID_IDispatch to get a dispatch interface that represents the <a href="https://msdn.microsoft.com/3b866266-fee0-42f7-a1e0-9adb6cc2e23f">ShellFolderView</a> object for the view.


### -field SVGIO_SELECTION

0x00000001. Refers to the currently selected items. Used with IID_IDataObject to retrieve a data object that represents the selected items.


### -field SVGIO_ALLVIEW

0x00000002. Used in the same way as <a href="https://msdn.microsoft.com/06ed616b-8121-4ea0-bd05-632888d0f376">SVGIO_SELECTION</a> but refers to all items in the view.


### -field SVGIO_CHECKED

0x00000003. Used in the same way as <a href="https://msdn.microsoft.com/06ed616b-8121-4ea0-bd05-632888d0f376">SVGIO_SELECTION</a> but refers to checked items in views where checked mode is supported. For more details on checked mode, see <a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>.


### -field SVGIO_TYPE_MASK

0x0000000F. Masks all bits but those corresponding to the <a href="https://msdn.microsoft.com/06ed616b-8121-4ea0-bd05-632888d0f376">_SVGIO</a> flags.


### -field SVGIO_FLAG_VIEWORDER

0x80000000. Returns the items in the order they appear in the view. If this flag is not set, the selected item will be listed first.


## -remarks



The <b>SVGIO</b> type used to refer to members of the <b>_SVGIO</b> enumeration is defined in Shobjidl.h as shown here.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef int SVGIO;</pre>
</td>
</tr>
</table></span></div>


