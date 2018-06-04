---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


