---
UID: NF:shellapi.SHGetFileInfoW
title: SHGetFileInfoW function (shellapi.h)
description: Retrieves information about an object in the file system, such as a file, folder, directory, or drive root. (Unicode)
helpviewer_keywords: ["SHGFI_ADDOVERLAYS", "SHGFI_ATTRIBUTES", "SHGFI_ATTR_SPECIFIED", "SHGFI_DISPLAYNAME", "SHGFI_EXETYPE", "SHGFI_ICON", "SHGFI_ICONLOCATION", "SHGFI_LARGEICON", "SHGFI_LINKOVERLAY", "SHGFI_OPENICON", "SHGFI_OVERLAYINDEX", "SHGFI_PIDL", "SHGFI_SELECTED", "SHGFI_SHELLICONSIZE", "SHGFI_SMALLICON", "SHGFI_SYSICONINDEX", "SHGFI_TYPENAME", "SHGFI_USEFILEATTRIBUTES", "SHGetFileInfo", "SHGetFileInfo function [Windows Shell]", "SHGetFileInfoW", "_win32_SHGetFileInfo", "shell.SHGetFileInfo", "shellapi/SHGetFileInfo", "shellapi/SHGetFileInfoW"]
old-location: shell\SHGetFileInfo.htm
tech.root: shell
ms.assetid: d662bedf-4be0-4528-8121-e7923a42bc67
ms.date: 12/05/2018
ms.keywords: SHGFI_ADDOVERLAYS, SHGFI_ATTRIBUTES, SHGFI_ATTR_SPECIFIED, SHGFI_DISPLAYNAME, SHGFI_EXETYPE, SHGFI_ICON, SHGFI_ICONLOCATION, SHGFI_LARGEICON, SHGFI_LINKOVERLAY, SHGFI_OPENICON, SHGFI_OVERLAYINDEX, SHGFI_PIDL, SHGFI_SELECTED, SHGFI_SHELLICONSIZE, SHGFI_SMALLICON, SHGFI_SYSICONINDEX, SHGFI_TYPENAME, SHGFI_USEFILEATTRIBUTES, SHGetFileInfo, SHGetFileInfo function [Windows Shell], SHGetFileInfoA, SHGetFileInfoW, _win32_SHGetFileInfo, shell.SHGetFileInfo, shellapi/SHGetFileInfo, shellapi/SHGetFileInfoA, shellapi/SHGetFileInfoW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetFileInfoW (Unicode) and SHGetFileInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetFileInfoW
 - shellapi/SHGetFileInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHGetFileInfo
 - SHGetFileInfoA
 - SHGetFileInfoW
---

# SHGetFileInfoW function


## -description

Retrieves information about an object in the file system, such as a file, folder, directory, or drive root.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a <b>null</b>-terminated string of maximum length MAX_PATH that contains the path and file name. Both absolute and relative paths are valid.
    
    					

If the <i>uFlags</i> parameter includes the <b>SHGFI_PIDL</b> flag, this parameter must be the address of an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (PIDL) structure that contains the list of item identifiers that uniquely identifies the file within the Shell's namespace. The PIDL must be a fully qualified PIDL. Relative PIDLs are not allowed.

If the <i>uFlags</i> parameter includes the <b>SHGFI_USEFILEATTRIBUTES</b> flag, this parameter does not have to be a valid file name. The function will proceed as if the file exists with the specified name and with the file attributes passed in the <i>dwFileAttributes</i> parameter. This allows you to obtain information about a file type by passing just the extension for <i>pszPath</i> and passing <b>FILE_ATTRIBUTE_NORMAL</b> in <i>dwFileAttributes</i>.

This string can use either short (the 8.3 form) or long file names.

### -param dwFileAttributes

Type: <b>DWORD</b>

A combination of one or more <a href="/windows/desktop/FileIO/retrieving-and-changing-file-attributes">file attribute flags</a> (FILE_ATTRIBUTE_ values as defined in Winnt.h). If <i>uFlags</i> does not include the <b>SHGFI_USEFILEATTRIBUTES</b> flag, this parameter is ignored.

### -param psfi [in, out]

Type: <b><a href="/windows/desktop/api/shellapi/ns-shellapi-shfileinfoa">SHFILEINFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileinfoa">SHFILEINFO</a> structure to receive the file information.

### -param cbFileInfo

Type: <b>UINT</b>

The size, in bytes, of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileinfoa">SHFILEINFO</a> structure pointed to by the <i>psfi</i> parameter.

### -param uFlags

Type: <b>UINT</b>

The flags that specify the file information to retrieve. This parameter can be a combination of the following values.



#### SHGFI_ADDOVERLAYS (0x000000020)


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Apply the appropriate overlays to the file's icon. The <b>SHGFI_ICON</b> flag must also be set.



#### SHGFI_ATTR_SPECIFIED (0x000020000)

Modify <b>SHGFI_ATTRIBUTES</b> to indicate that the <b>dwAttributes</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileinfoa">SHFILEINFO</a> structure at <i>psfi</i> contains the specific attributes that are desired. These attributes are passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>. If this flag is not specified, 0xFFFFFFFF is passed to <b>IShellFolder::GetAttributesOf</b>, requesting all attributes. This flag cannot be specified with the <b>SHGFI_ICON</b> flag.



#### SHGFI_ATTRIBUTES (0x000000800)

Retrieve the item attributes. The attributes are copied to the <b>dwAttributes</b> member of the structure specified in the <i>psfi</i> parameter. These are the same attributes that are obtained from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>.



#### SHGFI_DISPLAYNAME (0x000000200)

Retrieve the display name for the file, which is the name as it appears in Windows Explorer. The name is copied to the <b>szDisplayName</b> member of the structure specified in <i>psfi</i>. The returned display name uses the long file name, if there is one, rather than the 8.3 form of the file name. Note that the display name can be affected by settings such as whether extensions are shown.



#### SHGFI_EXETYPE (0x000002000)

Retrieve the type of the executable file if <i>pszPath</i> identifies an executable file. The information is packed into the return value. This flag cannot be specified with any other flags.



#### SHGFI_ICON (0x000000100)

Retrieve the handle to the icon that represents the file and the index of the icon within the system image list. The handle is copied to the <b>hIcon</b> member of the structure specified by <i>psfi</i>, and the index is copied to the <b>iIcon</b> member.



#### SHGFI_ICONLOCATION (0x000001000)

Retrieve the name of the file that contains the icon representing the file specified by <i>pszPath</i>, as returned by the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> method of the file's icon handler. Also retrieve the icon index within that file. The name of the file containing the icon is copied to the <b>szDisplayName</b> member of the structure specified by <i>psfi</i>. The icon's index is copied to that structure's <b>iIcon</b> member.



#### SHGFI_LARGEICON (0x000000000)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve the file's large icon. The <b>SHGFI_ICON</b> flag must also be set.



#### SHGFI_LINKOVERLAY (0x000008000)

Modify <b>SHGFI_ICON</b>, causing the function to add the link overlay to the file's icon. The <b>SHGFI_ICON</b> flag must also be set.



#### SHGFI_OPENICON (0x000000002)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve the file's open icon. Also used to modify <b>SHGFI_SYSICONINDEX</b>, causing the function to return the handle to the system image list that contains the file's small open icon. A container object displays an open icon to indicate that the container is open. The <b>SHGFI_ICON</b> and/or <b>SHGFI_SYSICONINDEX</b> flag must also be set.



#### SHGFI_OVERLAYINDEX (0x000000040)


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Return the index of the overlay icon. The value of the overlay index is returned in the upper eight bits of the <b>iIcon</b> member of the structure specified by <i>psfi</i>. This flag requires that the <b>SHGFI_ICON</b> be set as well.



#### SHGFI_PIDL (0x000000008)

Indicate that <i>pszPath</i> is the address of an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure rather than a path name.



#### SHGFI_SELECTED (0x000010000)

Modify <b>SHGFI_ICON</b>, causing the function to blend the file's icon with the system highlight color. The <b>SHGFI_ICON</b> flag must also be set.



#### SHGFI_SHELLICONSIZE (0x000000004)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve a Shell-sized icon. If this flag is not specified the function sizes the icon according to the system metric values. The <b>SHGFI_ICON</b> flag must also be set.



#### SHGFI_SMALLICON (0x000000001)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve the file's small icon. Also used to modify <b>SHGFI_SYSICONINDEX</b>, causing the function to return the handle to the system image list that contains small icon images. The <b>SHGFI_ICON</b> and/or <b>SHGFI_SYSICONINDEX</b> flag must also be set.



#### SHGFI_SYSICONINDEX (0x000004000)

Retrieve the index of a system image list icon. If successful, the index is copied to the <b>iIcon</b> member of <i>psfi</i>. The return value is a handle to the system image list. Only those images whose indices are successfully copied to <b>iIcon</b> are valid. Attempting to access other images in the system image list will result in undefined behavior.



#### SHGFI_TYPENAME (0x000000400)

Retrieve the string that describes the file's type. The string is copied to the <b>szTypeName</b> member of the structure specified in <i>psfi</i>.



#### SHGFI_USEFILEATTRIBUTES (0x000000010)

Indicates that the function should not attempt to access the file specified by <i>pszPath</i>. Rather, it should act as if the file specified by <i>pszPath</i> exists with the file attributes passed in <i>dwFileAttributes</i>. This flag cannot be combined with the <b>SHGFI_ATTRIBUTES</b>, <b>SHGFI_EXETYPE</b>, or <b>SHGFI_PIDL</b> flags.


##### - uFlags.SHGFI_ADDOVERLAYS (0x000000020)


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Apply the appropriate overlays to the file's icon. The <b>SHGFI_ICON</b> flag must also be set.


##### - uFlags.SHGFI_ATTRIBUTES (0x000000800)

Retrieve the item attributes. The attributes are copied to the <b>dwAttributes</b> member of the structure specified in the <i>psfi</i> parameter. These are the same attributes that are obtained from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>.


##### - uFlags.SHGFI_ATTR_SPECIFIED (0x000020000)

Modify <b>SHGFI_ATTRIBUTES</b> to indicate that the <b>dwAttributes</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileinfoa">SHFILEINFO</a> structure at <i>psfi</i> contains the specific attributes that are desired. These attributes are passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>. If this flag is not specified, 0xFFFFFFFF is passed to <b>IShellFolder::GetAttributesOf</b>, requesting all attributes. This flag cannot be specified with the <b>SHGFI_ICON</b> flag.


##### - uFlags.SHGFI_DISPLAYNAME (0x000000200)

Retrieve the display name for the file, which is the name as it appears in Windows Explorer. The name is copied to the <b>szDisplayName</b> member of the structure specified in <i>psfi</i>. The returned display name uses the long file name, if there is one, rather than the 8.3 form of the file name. Note that the display name can be affected by settings such as whether extensions are shown.


##### - uFlags.SHGFI_EXETYPE (0x000002000)

Retrieve the type of the executable file if <i>pszPath</i> identifies an executable file. The information is packed into the return value. This flag cannot be specified with any other flags.


##### - uFlags.SHGFI_ICON (0x000000100)

Retrieve the handle to the icon that represents the file and the index of the icon within the system image list. The handle is copied to the <b>hIcon</b> member of the structure specified by <i>psfi</i>, and the index is copied to the <b>iIcon</b> member.


##### - uFlags.SHGFI_ICONLOCATION (0x000001000)

Retrieve the name of the file that contains the icon representing the file specified by <i>pszPath</i>, as returned by the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> method of the file's icon handler. Also retrieve the icon index within that file. The name of the file containing the icon is copied to the <b>szDisplayName</b> member of the structure specified by <i>psfi</i>. The icon's index is copied to that structure's <b>iIcon</b> member.


##### - uFlags.SHGFI_LARGEICON (0x000000000)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve the file's large icon. The <b>SHGFI_ICON</b> flag must also be set.


##### - uFlags.SHGFI_LINKOVERLAY (0x000008000)

Modify <b>SHGFI_ICON</b>, causing the function to add the link overlay to the file's icon. The <b>SHGFI_ICON</b> flag must also be set.


##### - uFlags.SHGFI_OPENICON (0x000000002)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve the file's open icon. Also used to modify <b>SHGFI_SYSICONINDEX</b>, causing the function to return the handle to the system image list that contains the file's small open icon. A container object displays an open icon to indicate that the container is open. The <b>SHGFI_ICON</b> and/or <b>SHGFI_SYSICONINDEX</b> flag must also be set.


##### - uFlags.SHGFI_OVERLAYINDEX (0x000000040)


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Return the index of the overlay icon. The value of the overlay index is returned in the upper eight bits of the <b>iIcon</b> member of the structure specified by <i>psfi</i>. This flag requires that the <b>SHGFI_ICON</b> be set as well.


##### - uFlags.SHGFI_PIDL (0x000000008)

Indicate that <i>pszPath</i> is the address of an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure rather than a path name.


##### - uFlags.SHGFI_SELECTED (0x000010000)

Modify <b>SHGFI_ICON</b>, causing the function to blend the file's icon with the system highlight color. The <b>SHGFI_ICON</b> flag must also be set.


##### - uFlags.SHGFI_SHELLICONSIZE (0x000000004)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve a Shell-sized icon. If this flag is not specified the function sizes the icon according to the system metric values. The <b>SHGFI_ICON</b> flag must also be set.


##### - uFlags.SHGFI_SMALLICON (0x000000001)

Modify <b>SHGFI_ICON</b>, causing the function to retrieve the file's small icon. Also used to modify <b>SHGFI_SYSICONINDEX</b>, causing the function to return the handle to the system image list that contains small icon images. The <b>SHGFI_ICON</b> and/or <b>SHGFI_SYSICONINDEX</b> flag must also be set.


##### - uFlags.SHGFI_SYSICONINDEX (0x000004000)

Retrieve the index of a system image list icon. If successful, the index is copied to the <b>iIcon</b> member of <i>psfi</i>. The return value is a handle to the system image list. Only those images whose indices are successfully copied to <b>iIcon</b> are valid. Attempting to access other images in the system image list will result in undefined behavior.


##### - uFlags.SHGFI_TYPENAME (0x000000400)

Retrieve the string that describes the file's type. The string is copied to the <b>szTypeName</b> member of the structure specified in <i>psfi</i>.


##### - uFlags.SHGFI_USEFILEATTRIBUTES (0x000000010)

Indicates that the function should not attempt to access the file specified by <i>pszPath</i>. Rather, it should act as if the file specified by <i>pszPath</i> exists with the file attributes passed in <i>dwFileAttributes</i>. This flag cannot be combined with the <b>SHGFI_ATTRIBUTES</b>, <b>SHGFI_EXETYPE</b>, or <b>SHGFI_PIDL</b> flags.

## -returns

Type: <b>DWORD_PTR</b>

Returns a value whose meaning depends on the <i>uFlags</i> parameter. 
    
    					

If <i>uFlags</i> does not contain <b>SHGFI_EXETYPE</b> or <b>SHGFI_SYSICONINDEX</b>, the return value is nonzero if successful, or zero otherwise.

If <i>uFlags</i> contains the <b>SHGFI_EXETYPE</b> flag, the return value specifies the type of the executable file. It will be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Nonexecutable file or an error condition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LOWORD = NE or PE and HIWORD = Windows version</b></dt>
</dl>
</td>
<td width="60%">
Windows application.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LOWORD = MZ and HIWORD = 0</b></dt>
</dl>
</td>
<td width="60%">
MS-DOS .exe or .com file 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LOWORD = PE and HIWORD = 0</b></dt>
</dl>
</td>
<td width="60%">
Console application or .bat file 

</td>
</tr>
</table>

## -remarks

You should call this function from a background thread. Failure to do so could cause the UI to stop responding.

If <b>SHGetFileInfo</b> returns an icon handle in the <b>hIcon</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shfileinfoa">SHFILEINFO</a> structure pointed to by <i>psfi</i>, you are responsible for freeing it with <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> when you no longer need it.

<div class="alert"><b>Note</b>  Once you have a handle to a system image list, you can use the <a href="/windows/desktop/Controls/image-lists">Image List API</a> to manipulate it like any other image list. Because system image lists are created on a per-process basis, you should treat them as read-only objects. Writing to a system image list may overwrite or delete one of the system images, making it unavailable or incorrect for the remainder of the process.</div>
<div> </div>
You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> prior to calling <b>SHGetFileInfo</b>.

When you use the <b>SHGFI_EXETYPE</b> flag with a Windows application, the Windows version of the executable is given in the HIWORD of the return value. This version is returned as a hexadecimal value. For details on equating this value with a specific Windows version, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

The following code example uses <b>SHGetFileInfo</b> to retrieve the display name of the Recycle Bin, identified by its PIDL.


```cpp
LPITEMIDLIST pidl = NULL;
hr = SHGetFolderLocation(NULL, CSIDL_BITBUCKET, NULL, 0, &pidl);

if (SUCCEEDED(hr))                    
{
    SHFILEINFOW sfi = {0};
    hr = SHGetFileInfo((LPCTSTR)pidl,
                        -1,
                        &sfi,
                        sizeof(sfi),
                        SHGFI_PIDL | SHGFI_DISPLAYNAME)
            
    if (SUCCEEDED(hr))
    {
        // The display name is now held in sfi.szDisplayName.
    }
}

ILFree(pidl);
```






> [!NOTE]
> The shellapi.h header defines SHGetFileInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/shell/fileiconinit">FileIconInit</a>
