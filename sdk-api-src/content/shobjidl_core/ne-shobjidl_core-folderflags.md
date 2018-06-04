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

# FOLDERFLAGS enumeration


## -description


A set of flags that specify folder view options. The flags are independent of each other and can be used in any combination.


## -enum-fields




### -field FWF_NONE

0x00000000. <b>Windows 7 and later</b>. No special view options.


### -field FWF_AUTOARRANGE

0x00000001. Automatically arrange the elements in the view. This implies <a href="https://msdn.microsoft.com/8b57239b-112e-4fb6-b394-15501bd3f5b3">LVS_AUTOARRANGE</a> if the list-view control is used to implement the view.


### -field FWF_ABBREVIATEDNAMES

0x00000002. Not supported.


### -field FWF_SNAPTOGRID

0x00000004. Not supported.


### -field FWF_OWNERDATA

0x00000008. Not supported.


### -field FWF_BESTFITWINDOW

0x00000010. Not supported.


### -field FWF_DESKTOP

0x00000020. Make the folder behave like the desktop. This value applies only to the desktop and is not used for typical Shell folders. This flag implies <b>FWF_NOCLIENTEDGE</b> and <b>FWF_NOSCROLL</b>.


### -field FWF_SINGLESEL

0x00000040. Do not allow more than a single item to be selected. This is used in the common dialog boxes.


### -field FWF_NOSUBFOLDERS

0x00000080. Do not show subfolders.


### -field FWF_TRANSPARENT

0x00000100. Draw transparently. This is used only for the desktop.


### -field FWF_NOCLIENTEDGE

0x00000200. Not supported.


### -field FWF_NOSCROLL

0x00000400. Do not add scroll bars. This is used only for the desktop.


### -field FWF_ALIGNLEFT

0x00000800. The view should be left-aligned. This implies <a href="https://msdn.microsoft.com/8b57239b-112e-4fb6-b394-15501bd3f5b3">LVS_ALIGNLEFT</a> if the list-view control is used to implement the view.


### -field FWF_NOICONS

0x00001000. The view should not display icons.


### -field FWF_SHOWSELALWAYS

0x00002000. This flag is deprecated as of Windows XP and has no effect. Always show the selection.


### -field FWF_NOVISIBLE

0x00004000. Not supported.


### -field FWF_SINGLECLICKACTIVATE

0x00008000. Not supported.


### -field FWF_NOWEBVIEW

0x00010000. The view should not be shown as a web view.


### -field FWF_HIDEFILENAMES

0x00020000. The view should not display file names.


### -field FWF_CHECKSELECT

0x00040000. Turns on the check mode for the view.


### -field FWF_NOENUMREFRESH

0x00080000. <b>Windows Vista and later</b>. Do not re-enumerate the view (or drop the current contents of the view) when the view is refreshed.


### -field FWF_NOGROUPING

0x00100000. <b>Windows Vista and later</b>. Do not allow grouping in the view


### -field FWF_FULLROWSELECT

0x00200000. <b>Windows Vista and later</b>. When an item is selected, the item and all its sub-items are highlighted.


### -field FWF_NOFILTERS

0x00400000. <b>Windows Vista and later</b>. Do not display filters in the view.


### -field FWF_NOCOLUMNHEADER

0x00800000. <b>Windows Vista and later</b>. Do not display a column header in the view in any view mode.


### -field FWF_NOHEADERINALLVIEWS

0x01000000. <b>Windows Vista and later</b>. Only show the column header in details view mode.


### -field FWF_EXTENDEDTILES

0x02000000. <b>Windows Vista and later</b>. When the view is in "tile view mode" the layout of a single item should be extended to the width of the view.


### -field FWF_TRICHECKSELECT

0x04000000. <b>Windows Vista and later</b>. Not supported.


### -field FWF_AUTOCHECKSELECT

0x08000000. <b>Windows Vista and later</b>. Items can be selected using checkboxes.


### -field FWF_NOBROWSERVIEWSTATE

0x10000000. <b>Windows Vista and later</b>. The view should not save view state in the browser.


### -field FWF_SUBSETGROUPS

0x20000000. <b>Windows Vista and later</b>. The view should list the number of items displayed in each group.  To be used with <a href="https://msdn.microsoft.com/5aacc63a-d129-4539-a43f-f4dd74ab4fea">IFolderView2::SetGroupSubsetCount</a>.


### -field FWF_USESEARCHFOLDER

0x40000000. <b>Windows Vista and later</b>. Use the search folder for stacking and searching.


### -field FWF_ALLOWRTLREADING

(int)0x80000000. <b>Windows Vista and later</b>. Ensure right-to-left reading layout in a right-to-left system. Without this flag, the view displays strings from left-to-right both on systems set to left-to-right and right-to-left reading layout, which ensures that file names display correctly.

