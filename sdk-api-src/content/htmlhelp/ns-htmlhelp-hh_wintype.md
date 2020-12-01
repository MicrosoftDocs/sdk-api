---
UID: NS:htmlhelp.tagHH_WINTYPE
title: HH_WINTYPE (htmlhelp.h)
description: Use this structure to specify or modify the attributes of a window type.
helpviewer_keywords: ["*PHH_WINTYPE","HH_WINTYPE","HH_WINTYPE structure [HTML Help Workshop]","htmlhelp.hh_wintype_structure","htmlhelp/HH_WINTYPE","vsconStrhhwintype"]
old-location: htmlhelp\hh_wintype_structure.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhwintype.htm
ms.date: 12/05/2018
ms.keywords: '*PHH_WINTYPE, HH_WINTYPE, HH_WINTYPE structure [HTML Help Workshop], htmlhelp.hh_wintype_structure, htmlhelp/HH_WINTYPE, vsconStrhhwintype'
req.header: htmlhelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HH_WINTYPE, *PHH_WINTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHH_WINTYPE
 - htmlhelp/tagHH_WINTYPE
 - PHH_WINTYPE
 - htmlhelp/PHH_WINTYPE
 - HH_WINTYPE
 - htmlhelp/HH_WINTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HH_WINTYPE
---

# HH_WINTYPE structure


## -description

Use this structure to specify or modify the attributes of a <a href="/previous-versions/windows/desktop/legacy/ms644703(v=vs.85)">window type</a>.

## -struct-fields

### -field cbStruct

Specifies the size of the structure. This value must always be filled in before passing the structure to HtmlHelp().

### -field fUniCodeStrings

Specifies whether the strings used in this structure are UNICODE.

### -field pszType

A null-terminated string that specifies the name of the window type.

### -field fsValidMembers

Specifies which members in the structure are valid.

### -field fsWinProperties

Specifies the properties of the window, such as whether it is the standard HTML Help Viewer or whether it includes a Search tab.

### -field pszCaption

A null-terminated string that specifies the caption to display in the title bar of the window.

### -field dwStyles

Specifies the styles used to create the window. These styles can be ignored, combined with extended styles, or used exclusively depending on the value of the <i>fsValidMembers</i> and <i>fsWinProperties</i> parameters.

### -field dwExStyles

Specifies the extended styles used to create the window. These styles can be ignored, combined with default styles, or used exclusively depending on the value of the <i>fsValidMembers</i> and <i>fsWinProperties</i> parameters.

### -field rcWindowPos

Specifies the coordinates of the window in pixels. The values are read in the following order: 


<i>rcWindowPos</i> = {left, top, right, bottom};

### -field nShowState

Specifies the initial display state of the window. Valid values are the same as those for the Win32 API <b>ShowWindow</b> function.

### -field hwndHelp

Specifies the handle of the window if the window has been created.

### -field hwndCaller

Specifies the window that will receive HTML Help notification messages. <a href="/previous-versions/windows/desktop/htmlhelp/about-notification-messages">Notification messages</a> are sent via Windows <b>WM_NOTIFY</b> messages.

### -field paInfoTypes

Pointer to an array of Information Types.

### -field hwndToolBar

Specifies the handle of the toolbar.

### -field hwndNavigation

Specifies the handle of the Navigation pane.

### -field hwndHTML

Specifies the handle of the Topic pane, which hosts Shdocvw.dll.

### -field iNavWidth

Specifies the width of the Navigation pane when the Help Viewer is expanded.

### -field rcHTML

Specifies the coordinates of the Topic pane.

### -field pszToc

Specifies the contents (.hhc) file to display in the Navigation pane.

### -field pszIndex

Specifies the index (.hhk) file to display in the Navigation pane.

### -field pszFile

Specifies the default HTML file to display in the Topic pane.

### -field pszHome

Specifies the file or URL to display in the Topic pane when the Home button is clicked. 


Specifies which buttons to include on the toolbar.

### -field fsToolBarFlags

Specifies which buttons to include on the Toolbar pane of a three-pane Help Viewer.

### -field fNotExpanded

Specifies that the Help Viewer open with the Navigation pane closed.

### -field curNavType

Specifies the default tab to display on the Navigation pane.

### -field tabpos

Specifies where to place the tabs on the Navigation pane of the HTML Help Viewer.

### -field idNotify

Specifies a non-zero ID for enabling HTML Help notification messages. This ID is passed as the wParam value of Windows <b>WM_NOTIFY</b> messages.

### -field tabOrder

Tab order: Contents, Index, Search, History, Favorites, Reserved 1-5, Custom tabs

### -field cHistory

Number of history items to keep.  (Default: 30)

### -field pszJump1

Specifies the text to display underneath the Jump1 button.

### -field pszJump2

Specifies the text to display underneath the Jump2 button.

### -field pszUrlJump1

Specifies the URL to jump to when the Jump1 button is clicked.

### -field pszUrlJump2

Specifies the URL to jump to when the Jump2 button is clicked.

### -field rcMinSize

Minimum size for window (ignored in version 1).

### -field cbInfoTypes

Size of <i>paInfoTypes</i>

### -field pszCustomTabs

Series of zero-terminated strings to be used as tab labels.

## -remarks

Window types can be defined by an author in a project (.hhp) file, or they can be defined programmatically using the HTML Help API.

When a <b>HH_WINTYPE</b> structure is passed to <b>HtmlHelp()</b> using the <b>HH_SET_WIN_TYPE</b> command, the HTML Help API makes a private copy of the contents of the structure. The help developer is therefore responsible for freeing memory used by the <b>HH_WINTYPE</b> structure or character arrays within it. The help developer can free memory after calling <b>HH_SET_WIN_TYPE</b>.

<h3><a id="Used_by"></a><a id="used_by"></a><a id="USED_BY"></a>Used by</h3>
<ul>
<li>
<a href="/previous-versions/windows/desktop/htmlhelp/hh-set-win-type-command">HH_SET_WIN_TYPE</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/htmlhelp/hh-get-win-type-command">HH_GET_WIN_TYPE</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/htmlhelp/about-structures">About Structures</a>