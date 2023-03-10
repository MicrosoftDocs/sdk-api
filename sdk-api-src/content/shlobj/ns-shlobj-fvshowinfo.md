---
UID: NS:shlobj.FVSHOWINFO
title: FVSHOWINFO (shlobj.h)
description: Contains information that the file viewer uses to display a file.
helpviewer_keywords: ["*LPFVSHOWINFO","FVSHOWINFO","FVSHOWINFO structure [Windows Shell]","FVSIF_CANVIEWIT","FVSIF_NEWFAILED","FVSIF_NEWFILE","FVSIF_PINNED","FVSIF_RECT","LPFVSHOWINFO","LPFVSHOWINFO structure pointer [Windows Shell]","_win32_FVSHOWINFO","shell.FVSHOWINFO","shlobj/FVSHOWINFO","shlobj/LPFVSHOWINFO"]
old-location: shell\FVSHOWINFO.htm
tech.root: shell
ms.assetid: 8f399964-1ce4-4a9c-8cea-650a698783d3
ms.date: 12/05/2018
ms.keywords: '*LPFVSHOWINFO, FVSHOWINFO, FVSHOWINFO structure [Windows Shell], FVSIF_CANVIEWIT, FVSIF_NEWFAILED, FVSIF_NEWFILE, FVSIF_PINNED, FVSIF_RECT, LPFVSHOWINFO, LPFVSHOWINFO structure pointer [Windows Shell], _win32_FVSHOWINFO, shell.FVSHOWINFO, shlobj/FVSHOWINFO, shlobj/LPFVSHOWINFO'
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: FVSHOWINFO, *LPFVSHOWINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPFVSHOWINFO
 - shlobj/LPFVSHOWINFO
 - FVSHOWINFO
 - shlobj/FVSHOWINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - FVSHOWINFO
---

# FVSHOWINFO structure


## -description

Contains information that the file viewer uses to display a file.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes.

### -field hwndOwner

Type: <b>HWND</b>

A window handle to the owner of the window where the file will be displayed.

### -field iShow

Type: <b>int</b>

The show command for the window. This parameter is one of the <b>SW_</b> values detailed in <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>.

### -field dwFlags

Type: <b>DWORD</b>

Flags that determine what the file viewer displays. This member can be one or more of the following values.



#### FVSIF_CANVIEWIT

The file viewer can display the file.



#### FVSIF_NEWFAILED

The file viewer specified a new file to display, but no viewer could display the file. The file viewer should either continue to display the previous file or terminate.



#### FVSIF_NEWFILE

A drag-and-drop operation has dropped a file on the file viewer window. The file viewer passes the name of the file to the Shell by copying the name to the <b>strNewFile</b> member. The Shell attempts to load a file viewer that can display the new file.



#### FVSIF_PINNED

A pinned window exists. A file viewer should either use the pinned window to display the file or set a new pinned window and display the file in it.



#### FVSIF_RECT

The <b>rect</b> member contains valid data.

### -field rect

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the size and position of the file viewer's window. This member is valid only if the <b>dwFlags</b> member includes the <b>FVSIF_RECT</b> value.

### -field punkRel

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The address of an interface that has its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method called by a new file viewer to release the previous file viewer. This member is used when a drag-and-drop operation drops a file on the file viewer's window.

### -field strNewFile

Type: <b>OLECHAR[MAX_PATH]</b>

The address of a string that specifies the name of a new file to display. A file viewer sets this member when a drag-and-drop operation drops a file on the file viewer's window.

