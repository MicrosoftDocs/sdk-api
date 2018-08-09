---
UID: NS:shlobj_core._FILEDESCRIPTORA
title: "_FILEDESCRIPTORA"
author: windows-sdk-content
description: Describes the properties of a file that is being copied by means of the clipboard during a Microsoft ActiveX drag-and-drop operation.
old-location: shell\FILEDESCRIPTOR.htm
old-project: shell
ms.assetid: b81a7e52-5bd8-4fa4-bd76-9a58afaceec0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPFILEDESCRIPTORA, FD_ACCESSTIME, FD_ATTRIBUTES, FD_CLSID, FD_CREATETIME, FD_FILESIZE, FD_LINKUI, FD_PROGRESSUI, FD_SIZEPOINT, FD_UNICODE, FD_WRITESTIME, FILEDESCRIPTOR, FILEDESCRIPTOR structure [Windows Shell], FILEDESCRIPTORA, LPFILEDESCRIPTOR, LPFILEDESCRIPTOR structure pointer [Windows Shell], _FILEDESCRIPTORA, _FILEDESCRIPTORW, _win32_FILEDESCRIPTOR, shell.FILEDESCRIPTOR, shlobj_core/FILEDESCRIPTOR, shlobj_core/LPFILEDESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
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
tech.root: 
req.typenames: FILEDESCRIPTORA, *LPFILEDESCRIPTORA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj_core.h
api_name:
 - FILEDESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _FILEDESCRIPTORA structure


## -description


Describes the properties of a file that is being copied by means of the clipboard during a Microsoft ActiveX <a href="https://msdn.microsoft.com/bd73098b-2f69-48a4-bb06-e1e0a452e69d">drag-and-drop</a> operation.


## -struct-fields




### -field dwFlags

Type: <b>DWORD</b>

An array of flags that indicate which of the other structure members contain valid data. This member can be a combination of the following values.



#### FD_CLSID (0x00000001)

0x00000001. The <b>clsid</b> member is valid.



#### FD_SIZEPOINT (0x00000002)

0x00000002. The <b>sizel</b> and <b>pointl</b> members are valid.



#### FD_ATTRIBUTES (0x00000004)

0x00000004. The <b>dwFileAttributes</b> member is valid.



#### FD_CREATETIME (0x00000008)

0x00000008. The <b>ftCreationTime</b> member is valid.



#### FD_ACCESSTIME (0x00000010)

0x00000010. The <b>ftLastAccessTime</b> member is valid.



#### FD_WRITESTIME (0x00000020)

0x00000020. The <b>ftLastWriteTime</b> member is valid.



#### FD_FILESIZE (0x00000040)

0x00000040. The <b>nFileSizeHigh</b> and <b>nFileSizeLow</b> members are valid.



#### FD_PROGRESSUI (0x00004000)

0x00004000. A progress indicator is shown with drag-and-drop operations.



#### FD_LINKUI (0x00008000)

0x00008000. Treat the operation as a shortcut.



#### FD_UNICODE ((int)0x80000000)

(int)0x80000000. <b>Windows Vista and later</b>. The descriptor is Unicode.


### -field clsid

Type: <b>CLSID</b>

The file type identifier.


### -field sizel

Type: <b>SIZEL</b>

The width and height of the file icon.


### -field pointl

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a></b>

The screen coordinates of the file object.


### -field dwFileAttributes

Type: <b>DWORD</b>

File attribute flags. This will be a combination of the FILE_ATTRIBUTE_ values described in <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>.


### -field ftCreationTime

Type: <b>FILETIME</b>

The <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time of file creation.


### -field ftLastAccessTime

Type: <b>FILETIME</b>

The <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time that the file was last accessed.


### -field ftLastWriteTime

Type: <b>FILETIME</b>

The <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time of the last write operation.


### -field nFileSizeHigh

Type: <b>DWORD</b>

The high-order <b>DWORD</b> of the file size, in bytes.


### -field nFileSizeLow

Type: <b>DWORD</b>

The low-order <b>DWORD</b> of the file size, in bytes.


### -field cFileName

Type: <b>TCHAR[MAX_PATH]</b>

The null-terminated string that contains the name of the file.


## -remarks



If the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_FILECONTENTS</a> format that corresponds to this structure contains the file as a global memory object, <b>nFileSizeHigh</b> and <b>nFileSizeLow</b> specify the size of the associated memory block. If they are set, they can also be used if a user-interface needs to be displayed. For example, if a file is about to be overwritten, you would typically use information from this structure to display a dialog box containing the size, data, and name of the file.

To create a zero-length file, set the <b>FD_FILESIZE</b> flag in the <b>dwFlags</b>, and set <b>nFileSizeHigh</b> and <b>nFileSizeLow</b> to zero. The <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_FILECONTENTS</a> format should represent the file as either a stream or global memory object (<a href="https://msdn.microsoft.com/ac41286f-7c67-444a-81b7-21b61079bbf5">TYMED_ISTREAM</a> or <a href="https://msdn.microsoft.com/ac41286f-7c67-444a-81b7-21b61079bbf5">TYMED_HGLOBAL</a>).



