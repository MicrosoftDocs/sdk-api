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

The show command for the window. This parameter is one of the <b>SW_</b> values detailed in <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>.


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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the size and position of the file viewer's window. This member is valid only if the <b>dwFlags</b> member includes the <b>FVSIF_RECT</b> value.


### -field punkRel

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The address of an interface that has its <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method called by a new file viewer to release the previous file viewer. This member is used when a drag-and-drop operation drops a file on the file viewer's window.


### -field strNewFile

Type: <b>OLECHAR[MAX_PATH]</b>

The address of a string that specifies the name of a new file to display. A file viewer sets this member when a drag-and-drop operation drops a file on the file viewer's window.

