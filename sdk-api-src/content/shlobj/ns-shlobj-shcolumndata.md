---
UID: NS:shlobj.SHCOLUMNDATA
title: SHCOLUMNDATA (shlobj.h)
description: Contains information that identifies a particular file. It is used by IColumnProvider::GetItemData when requesting data for a particular file.
helpviewer_keywords: ["*LPSHCOLUMNDATA","FILE_ATTRIBUTE_ARCHIVE","FILE_ATTRIBUTE_COMPRESSED","FILE_ATTRIBUTE_DIRECTORY","FILE_ATTRIBUTE_ENCRYPTED","FILE_ATTRIBUTE_HIDDEN","FILE_ATTRIBUTE_NORMAL","FILE_ATTRIBUTE_OFFLINE","FILE_ATTRIBUTE_READONLY","FILE_ATTRIBUTE_REPARSE_POINT","FILE_ATTRIBUTE_SPARSE_FILE","FILE_ATTRIBUTE_SYSTEM","FILE_ATTRIBUTE_TEMPORARY","LPSHCOLUMNDATA","LPSHCOLUMNDATA structure pointer [Windows Shell]","SHCDF_UPDATEITEM","SHCOLUMNDATA","SHCOLUMNDATA structure [Windows Shell]","_win32_SHCOLUMNDATA_str","shell.SHCOLUMNDATA_str","shlobj/LPSHCOLUMNDATA","shlobj/SHCOLUMNDATA"]
old-location: shell\SHCOLUMNDATA_str.htm
tech.root: shell
ms.assetid: 3a0c9231-2871-4314-9db3-7e5609e08359
ms.date: 12/05/2018
ms.keywords: '*LPSHCOLUMNDATA, FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_REPARSE_POINT, FILE_ATTRIBUTE_SPARSE_FILE, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, LPSHCOLUMNDATA, LPSHCOLUMNDATA structure pointer [Windows Shell], SHCDF_UPDATEITEM, SHCOLUMNDATA, SHCOLUMNDATA structure [Windows Shell], _win32_SHCOLUMNDATA_str, shell.SHCOLUMNDATA_str, shlobj/LPSHCOLUMNDATA, shlobj/SHCOLUMNDATA'
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SHCOLUMNDATA, *LPSHCOLUMNDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPSHCOLUMNDATA
 - shlobj/LPSHCOLUMNDATA
 - SHCOLUMNDATA
 - shlobj/SHCOLUMNDATA
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
 - SHCOLUMNDATA
---

# SHCOLUMNDATA structure


## -description

Contains information that identifies a particular file. It is used by <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata">IColumnProvider::GetItemData</a> when requesting data for a particular file.

## -struct-fields

### -field dwFlags

Type: <b>ULONG</b>

Flags used to specify the nature of the request.



#### SHCDF_UPDATEITEM

The file specified by <b>wszFile</b> is a new file or a file that has changed since the last call to <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata">IColumnProvider::GetItemData</a>. Any cached data should be flushed and recalculated. Column handlers that do not cache data, or that display data that is stored separately from the file, can ignore this flag.

### -field dwFileAttributes

Type: <b>DWORD</b>

File attribute flags. It will be one or more of the following values.



#### FILE_ATTRIBUTE_ARCHIVE

The file or directory is an archive file or directory. Applications use this attribute to mark files for backup or removal.



#### FILE_ATTRIBUTE_COMPRESSED

The file or directory is compressed. For a file, this means that all data in the file is compressed. For a directory, this means that compression is the default for newly created files and subdirectories.



#### FILE_ATTRIBUTE_DIRECTORY

The handle identifies a directory.



#### FILE_ATTRIBUTE_ENCRYPTED

The file or directory is encrypted. For a file, this means that all data streams in the file are encrypted. For a directory, this means that encryption is the default for newly created files and subdirectories.



#### FILE_ATTRIBUTE_HIDDEN

The file or directory is hidden. It is not included in an ordinary directory listing.



#### FILE_ATTRIBUTE_NORMAL

The file or directory has no other attributes set. This attribute is valid only if used alone.



#### FILE_ATTRIBUTE_OFFLINE

The data of the file is not immediately available. This attribute indicates that the file data has been physically moved to offline storage. This attribute is used by Remote Storage, the hierarchical storage management software in Windows 2000. If this attribute is set, the column handler should avoid opening the file because doing so will cause the file to be recalled from offline storage.



#### FILE_ATTRIBUTE_READONLY

The file or directory is read-only. Applications can read the file but cannot write to it or delete it. In the case of a directory, applications cannot delete it.



#### FILE_ATTRIBUTE_REPARSE_POINT

The file has an associated reparse point.



#### FILE_ATTRIBUTE_SPARSE_FILE

The file is a sparse file.



#### FILE_ATTRIBUTE_SYSTEM

The file or directory is part of, or is used exclusively by, the operating system.



#### FILE_ATTRIBUTE_TEMPORARY

The file is being used for temporary storage. File systems attempt to keep all of the data in memory for quicker access rather than flushing the data back to mass storage. A temporary file should be deleted by the application as soon as it is no longer needed.

### -field dwReserved

Type: <b>ULONG</b>

Reserved. Set to <b>NULL</b>.

### -field pwszExt

Type: <b>WCHAR*</b>

A pointer to a null-terminated Unicode string with a file name extension.

### -field wszFile

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string containing a fully qualified file path.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>

