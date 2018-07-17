---
UID: NE:shobjidl_core._NSTCSTYLE
title: "_NSTCSTYLE"
author: windows-sdk-content
description: Describes the characteristics of a given namespace tree control.
old-location: shell\NSTCSTYLE.htm
old-project: shell
ms.assetid: 879af1be-2eea-4ebd-b9ea-64b1db40682d
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: NSTCSTYLE, NSTCSTYLE enumeration [Windows Shell], NSTCS_ALLOWJUNCTIONS, NSTCS_AUTOHSCROLL, NSTCS_BORDER, NSTCS_CHECKBOXES, NSTCS_DIMMEDCHECKBOXES, NSTCS_DISABLEDRAGDROP, NSTCS_EMPTYTEXT, NSTCS_EVENHEIGHT, NSTCS_EXCLUSIONCHECKBOXES, NSTCS_FADEINOUTEXPANDOS, NSTCS_FAVORITESMODE, NSTCS_FULLROWSELECT, NSTCS_HASEXPANDOS, NSTCS_HASLINES, NSTCS_HORIZONTALSCROLL, NSTCS_NOEDITLABELS, NSTCS_NOINDENTCHECKS, NSTCS_NOINFOTIP, NSTCS_NOORDERSTREAM, NSTCS_NOREPLACEOPEN, NSTCS_PARTIALCHECKBOXES, NSTCS_RICHTOOLTIP, NSTCS_ROOTHASEXPANDO, NSTCS_SHOWDELETEBUTTON, NSTCS_SHOWREFRESHBUTTON, NSTCS_SHOWSELECTIONALWAYS, NSTCS_SHOWTABSBUTTON, NSTCS_SINGLECLICKEXPAND, NSTCS_SPRINGEXPAND, NSTCS_TABSTOP, _NSTCSTYLE, _shell_NSTCSTYLE, shell.NSTCSTYLE, shobjidl_core/NSTCSTYLE, shobjidl_core/NSTCS_ALLOWJUNCTIONS, shobjidl_core/NSTCS_AUTOHSCROLL, shobjidl_core/NSTCS_BORDER, shobjidl_core/NSTCS_CHECKBOXES, shobjidl_core/NSTCS_DIMMEDCHECKBOXES, shobjidl_core/NSTCS_DISABLEDRAGDROP, shobjidl_core/NSTCS_EMPTYTEXT, shobjidl_core/NSTCS_EVENHEIGHT, shobjidl_core/NSTCS_EXCLUSIONCHECKBOXES, shobjidl_core/NSTCS_FADEINOUTEXPANDOS, shobjidl_core/NSTCS_FAVORITESMODE, shobjidl_core/NSTCS_FULLROWSELECT, shobjidl_core/NSTCS_HASEXPANDOS, shobjidl_core/NSTCS_HASLINES, shobjidl_core/NSTCS_HORIZONTALSCROLL, shobjidl_core/NSTCS_NOEDITLABELS, shobjidl_core/NSTCS_NOINDENTCHECKS, shobjidl_core/NSTCS_NOINFOTIP, shobjidl_core/NSTCS_NOORDERSTREAM, shobjidl_core/NSTCS_NOREPLACEOPEN, shobjidl_core/NSTCS_PARTIALCHECKBOXES, shobjidl_core/NSTCS_RICHTOOLTIP, shobjidl_core/NSTCS_ROOTHASEXPANDO, shobjidl_core/NSTCS_SHOWDELETEBUTTON, shobjidl_core/NSTCS_SHOWREFRESHBUTTON, shobjidl_core/NSTCS_SHOWSELECTIONALWAYS, shobjidl_core/NSTCS_SHOWTABSBUTTON, shobjidl_core/NSTCS_SINGLECLICKEXPAND, shobjidl_core/NSTCS_SPRINGEXPAND, shobjidl_core/NSTCS_TABSTOP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - NSTCSTYLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _NSTCSTYLE enumeration


## -description


Describes the characteristics of a given namespace tree control.


## -enum-fields




### -field NSTCS_HASEXPANDOS

The control displays a triangle—known as an expando—on the leftmost edge of those items that have child items. Clicking on the expando expands the item to reveal the children of the item. Has no effect when combined with NSTCS_SHOWTABSBUTTON, NSTCS_SHOWDELETEBUTTON, or NSTCS_SHOWREFRESHBUTTON.

                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_HASBUTTONS</a> tree view control style.


### -field NSTCS_HASLINES

The control draws lines to the left of the tree items that lead to their individual parent items. Has no effect when combined with NSTCS_SHOWTABSBUTTON, NSTCS_SHOWDELETEBUTTON, or NSTCS_SHOWREFRESHBUTTON.
                    
                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_HASLINES</a> tree view control style.


### -field NSTCS_SINGLECLICKEXPAND

An item expands to show its child items in response to a single mouse click.
                    
                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_SINGLEEXPAND</a> tree view control style.


### -field NSTCS_FULLROWSELECT

The selection of an item fills the row with inverse text to the end of the window area, regardless of the length of the text. When this option is not declared, only the area behind text is inverted. This value cannot be combined with NSTCS_HASLINES.

                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_FULLROWSELECT</a> tree view control style.


### -field NSTCS_SPRINGEXPAND

When one item is selected and expanded and you select a second item, the first selection automatically collapses.
                        

This is the opposite of the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_NOSINGLECOLLAPSE</a> tree view control style.


### -field NSTCS_HORIZONTALSCROLL

The area of the window that contains the tree of namespace items has a horizontal scroll bar.
                    
                        

Maps to the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_HSCROLL</a> Windows style.


### -field NSTCS_ROOTHASEXPANDO

The root item is preceded by an expando that allows expansion of the root item.
                    
                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_LINESATROOT</a> tree view control style.


### -field NSTCS_SHOWSELECTIONALWAYS

The node of an item is outlined when the control does not have the focus.
                    
                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_SHOWSELALWAYS</a> tree view control style.


### -field NSTCS_NOINFOTIP

Do not display infotips when the mouse cursor is over an item.
                    
                        

This is the opposite of the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_INFOTIP</a> tree view control style.


### -field NSTCS_EVENHEIGHT

Sets the height of the items to an even height. By default, the height of items can be even or odd.
                    
                        

This is the opposite of the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_NONEVENHEIGHT</a> tree view control style.


### -field NSTCS_NOREPLACEOPEN

Do not replace the <b>Open</b> command in the shortcut menu with a user-defined function.


### -field NSTCS_DISABLEDRAGDROP

Do not allow drag-and-drop operations within the control. Note that you can still drag an item from outside of the control and drop it onto the control.

                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_DISABLEDRAGDROP</a> tree view control style.


### -field NSTCS_NOORDERSTREAM

Do not persist reordering changes. Used with NSTCS_FAVORITESMODE. If favorites mode is not specified, this flag has no effect.


### -field NSTCS_RICHTOOLTIP

Use a rich tooltip. Rich tooltips display the item's icon in addition to the item's text. A standard tooltip displays only the item's text. The tree view displays tooltips only for items in the tree that are partially visible.

                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_RICHTOOLTIP</a> tree view control style.

NSTCS_RICHTOOLTIP has no effect unless it is combined with NSTCS_NOINFOTIP and/or NSTCS_FAVORITESMODE. If NSTCS_NOINFOTIP is not specified, the tree view displays an infotip instead of a tooltip. If NSTCS_FAVORITESMODE is not specified, the namespace tree control always sets the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_RICHTOOLTIP</a> style.


### -field NSTCS_BORDER

Draw a thin border around the control. Corresponds to <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_BORDER</a>.


### -field NSTCS_NOEDITLABELS

Do not allow creation of an in-place edit box, which would allow the user to rename the given item.
                    
                        

This is the opposite of the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_EDITLABELS</a> tree view control style.


### -field NSTCS_TABSTOP

If the control is hosted, you can tabstop into the control. Corresponds to <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">WS_EX_CONTROLPARENT</a>.


### -field NSTCS_FAVORITESMODE

The control has the appearance of the favorites band in Windows XP.


### -field NSTCS_AUTOHSCROLL

When you hover the mouse pointer over an item that extends past the end of the control window, the control automatically scrolls horizontally so that the item appears more fully in the window area.

                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_AUTOHSCROLL</a> tree view control style.


### -field NSTCS_FADEINOUTEXPANDOS

If the control does not have the focus and there are items that are preceded by expandos, then these expandos are visible only when the mouse pointer is near to the control.

                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_FADEINOUTEXPANDOS</a> tree view control style.


### -field NSTCS_EMPTYTEXT

If an item has no children and is not expanded, then that item contains a line of text at the child level that says "empty".


### -field NSTCS_CHECKBOXES

Items have check boxes on their leftmost side. These check boxes can be of types partial, exclusion or dimmed, which correspond to the flags NSTCS_PARTIALCHECKBOXES, NSTCS_EXCLUSIONCHECKBOXES, and NSTCS_DIMMEDCHECKBOXES.

                        

Maps to the <a href="https://msdn.microsoft.com/d0a1ad6d-1bda-4b65-b97a-b389d6e6d7a6">TVS_CHECKBOXES</a> tree view control style.


### -field NSTCS_PARTIALCHECKBOXES

Adds a checkbox icon on the leftmost side of a given item with a square in the center, that indicates that the node is partially selected. Must be combined with NSTCS_CHECKBOXES.

                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_PARTIALCHECKBOXES</a> tree view control style.


### -field NSTCS_EXCLUSIONCHECKBOXES

Adds a checkbox icon on the leftmost side of a given item that contains a red <b>X</b>, which indicates that the item is excluded from the current selection. Without this exclusion icon, selection of a parent item includes selection of its child items. Must be combined with NSTCS_CHECKBOXES.

                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_EXCLUSIONCHECKBOXES</a> tree view control style.


### -field NSTCS_DIMMEDCHECKBOXES

Adds a checkbox on the leftmost side of a given item that contains an icon of a dimmed check mark, that indicates that a node is selected because its parent is selected. Must be combined with NSTCS_CHECKBOXES.

                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_DIMMEDCHECKBOXES</a> tree view control style.


### -field NSTCS_NOINDENTCHECKS

Check boxes are located at the far left edge of the window area instead of being indented.
                    
                        

Maps to the <a href="https://msdn.microsoft.com/b45e7b7c-2c7b-49fa-8679-57c478b2f796">TVS_EX_NOINDENTSTATE</a> tree view control style.


### -field NSTCS_ALLOWJUNCTIONS

Allow junctions. A junction point, or just junction, is a root of a namespace extension that is normally displayed by Windows Explorer as a folder in both tree and folder views. For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.
                    
                     

Junctions exist in the file system as files, but are not treated as files. An example is a compressed file with a .zip file name extension, which to the file system is just a file. However, if this file is treated as a junction, it can represent an entire namespace. This allows the namespace tree control to treat compressed files and similar junctions as folders rather than as files.


### -field NSTCS_SHOWTABSBUTTON

Displays an arrow on the right side of an item if the item is a folder. The action associated with the arrow is implementation specific. Cannot be combined with NSTCS_SHOWDELETEBUTTON or NSTCS_SHOWREFRESHBUTTON.


### -field NSTCS_SHOWDELETEBUTTON

Displays a red <b>X</b> on the right side of an item. The action associated with the <b>X</b> is implementation specific. Cannot be combined with NSTCS_SHOWTABSBUTTON or NSTCS_SHOWREFRESHBUTTON.


### -field NSTCS_SHOWREFRESHBUTTON

Displays a refresh button on the right side of an item. The action associated with the button is implementation specific. Cannot be combined with NSTCS_SHOWTABSBUTTON or NSTCS_SHOWDELETEBUTTON.


## -remarks



Three values have effect only in conjunction with NSTCS_CHECKBOXES: NSTCS_PARTIALCHECKBOXES, NSTCS_EXCLUSIONCHECKBOXES, and NSTCS_DIMMEDCHECKBOXES. The icons associated with these states are inserted into the state image list as follows:




<table class="clsStd">
<tr>
<th>Image Slot</th>
<th>Image</th>
<th>Associated Flags</th>
</tr>
<tr>
<td>0</td>
<td>Blank</td>
<td>NSTCS_CHECKBOXES</td>
</tr>
<tr>
<td>1</td>
<td>Unchecked</td>
<td>NSTCS_CHECKBOXES</td>
</tr>
<tr>
<td>2</td>
<td>Checked</td>
<td>NSTCS_CHECKBOXES</td>
</tr>
<tr>
<td>3</td>
<td>Partial</td>
<td>NSTCS_CHECKBOXES | NSTCS_PARTIALCHECKBOXES</td>
</tr>
<tr>
<td>4</td>
<td>Exclusion (red X)</td>
<td>NSTCS_CHECKBOXES | NSTCS_EXCLUSIONCHECKBOXES</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/5305d7ba-e37f-4f95-8ae2-e0532012cb1e">INameSpaceTreeControl2::GetControlStyle</a>



<a href="https://msdn.microsoft.com/20a212e2-13e8-4e17-a8d3-78fff2a1fafb">INameSpaceTreeControl2::SetControlStyle</a>



<a href="https://msdn.microsoft.com/dfc602bd-6e4e-492d-8bf4-1499319adee7">INameSpaceTreeControl::Initialize</a>
 

 

