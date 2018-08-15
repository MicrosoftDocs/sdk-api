---
UID: NE:shobjidl_core._SVSIF
title: "_SVSIF"
author: windows-sdk-content
description: Indicates flags used by IFolderView, IFolderView2, IShellView and IShellView2 to specify a type of selection to apply.
old-location: shell\SVSIF.htm
old-project: shell
ms.assetid: 3b0a7ec3-f365-48ec-86b0-ffd4c345deaf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SVSI_CHECK, SVSI_CHECK2, SVSI_DESELECT, SVSI_DESELECTOTHERS, SVSI_EDIT, SVSI_ENSUREVISIBLE, SVSI_FOCUSED, SVSI_KEYBOARDSELECT, SVSI_NOTAKEFOCUS, SVSI_POSITIONITEM, SVSI_SELECT, SVSI_SELECTIONMARK, SVSI_TRANSLATEPT, _SVSIF, _SVSIF enumeration [Windows Shell], _shell_SVSIF, shell.SVSIF, shobjidl_core/SVSI_CHECK, shobjidl_core/SVSI_CHECK2, shobjidl_core/SVSI_DESELECT, shobjidl_core/SVSI_DESELECTOTHERS, shobjidl_core/SVSI_EDIT, shobjidl_core/SVSI_ENSUREVISIBLE, shobjidl_core/SVSI_FOCUSED, shobjidl_core/SVSI_KEYBOARDSELECT, shobjidl_core/SVSI_NOTAKEFOCUS, shobjidl_core/SVSI_POSITIONITEM, shobjidl_core/SVSI_SELECT, shobjidl_core/SVSI_SELECTIONMARK, shobjidl_core/SVSI_TRANSLATEPT, shobjidl_core/_SVSIF
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: "_SVSIF"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - _SVSIF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SVSIF enumeration


## -description


Indicates flags used by <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>, <a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a>, <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> and  <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a> to specify a type of selection to apply.


## -enum-fields




### -field SVSI_DESELECT

0x00000000. Deselect the item.


### -field SVSI_SELECT

0x00000001. Select the item.


### -field SVSI_EDIT

0x00000003. Put the name of the item into rename mode. This value includes SVSI_SELECT.


### -field SVSI_DESELECTOTHERS

0x00000004. Deselect all but the selected item. If the item parameter is <b>NULL</b>, deselect all items.


### -field SVSI_ENSUREVISIBLE

0x00000008. In the case of a folder that cannot display all of its contents on one screen, display the portion that contains the selected item.


### -field SVSI_FOCUSED

0x00000010. Give the selected item the focus when multiple items are selected, placing the item first in any list of the collection returned by a method.


### -field SVSI_TRANSLATEPT

0x00000020. Convert the input point from screen coordinates to the list-view client coordinates.


### -field SVSI_SELECTIONMARK

0x00000040. Mark the item so that it can be queried using <a href="https://msdn.microsoft.com/86416704-c2e3-4782-a566-b49cbd0e7696">IFolderView::GetSelectionMarkedItem</a>.


### -field SVSI_POSITIONITEM

0x00000080. Allows the window's default view to position the item. In most cases, this will place the item in the first available position. However, if the call comes during the processing of a mouse-positioned context menu, the position of the context menu is used to position the item.


### -field SVSI_CHECK

0x00000100. The item should be checked. This flag is used with items in views where the checked mode is supported.


### -field SVSI_CHECK2

0x00000200. The second check state when the view is in tri-check mode, in which there are three values for the checked state. You can indicate tri-check mode by specifying FWF_TRICHECKSELECT in <a href="https://msdn.microsoft.com/94999ac7-c9dd-439e-8f63-eeb226763200">IFolderView2::SetCurrentFolderFlags</a>. The 3 states for FWF_TRICHECKSELECT are unchecked, SVSI_CHECK and SVSI_CHECK2.


### -field SVSI_KEYBOARDSELECT

0x00000401. Selects the item and marks it as selected by the keyboard. This value includes SVSI_SELECT.


### -field SVSI_NOTAKEFOCUS

0x40000000. An operation to select or focus an item should not also set focus on the view itself.


## -remarks



An additional value SVSI_NOSTATECHANGE is also defined outside of the enumeration. This value indicates that an operation to edit or position an item should not affect the item's focus or selected state. Its numeric value is (UINT)0x80000000.

The <b>SVSIF</b> type used to refer to members of the <b>_SVSIF</b> enumeration is defined in Shobjidl.h as shown here.

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef UINT SVSIF;</pre>
</td>
</tr>
</table></span></div>


