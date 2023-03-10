---
UID: NF:shobjidl_core.IShellLibrary.GetFolders
title: IShellLibrary::GetFolders (shobjidl_core.h)
description: Gets the set of child folders that are contained in the library.
helpviewer_keywords: ["GetFolders","GetFolders method [Windows Shell]","GetFolders method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","GetFolders method","IShellLibrary.GetFolders","IShellLibrary::GetFolders","LFF_ALLITEMS","LFF_FORCEFILESYSTEM","LFF_STORAGEITEMS","_shell_IShellLibrary_GetFolders","shell.IShellLibrary_GetFolders","shobjidl_core/IShellLibrary::GetFolders"]
old-location: shell\IShellLibrary_GetFolders.htm
tech.root: shell
ms.assetid: 19abc4f9-5123-4dd9-9606-21b52e28854b
ms.date: 12/05/2018
ms.keywords: GetFolders, GetFolders method [Windows Shell], GetFolders method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetFolders method, IShellLibrary.GetFolders, IShellLibrary::GetFolders, LFF_ALLITEMS, LFF_FORCEFILESYSTEM, LFF_STORAGEITEMS, _shell_IShellLibrary_GetFolders, shell.IShellLibrary_GetFolders, shobjidl_core/IShellLibrary::GetFolders
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLibrary::GetFolders
 - shobjidl_core/IShellLibrary::GetFolders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.GetFolders
---

# IShellLibrary::GetFolders


## -description

Gets the set of child folders that are contained in the library.

## -parameters

### -param lff [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter">LIBRARYFOLDERFILTER</a></b>

One of the following <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter">LIBRARYFOLDERFILTER</a>   values that determines the folders to get. These flags cannot be combined.



#### LFF_FORCEFILESYSTEM (1)

Get only file-system folders. File-system folders  are  folders that have the  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">SFGAO_FILESYSTEM</a>  attribute set.



#### LFF_STORAGEITEMS (2)

Get all folders that can be bound to <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> objects.  These folders  are   folders that have the  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">SFGAO_STORAGE</a>  or  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">SFGAO_FILESYSTEM</a> attribute set.



#### LFF_ALLITEMS (3)

Get all folders in the library.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to  get in  <i>ppv</i>. This value is typically IID_IShellItemArray,  but it can also be IID_IObjectCollection, IID_IObjectArray, or the IID of any other interface that is implemented by CShellItemArray.

### -param ppv [out]

Type: <b>void**</b>

 A pointer to the interface  requested in <i>riid</i>. If this  call fails, this value is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call was successful and the specified folders were returned in <i>ppv</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The call was successful but not all specified folders were returned in <i>ppv</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_</b></dt>
</dl>
</td>
<td width="60%">
This method can return other error values.

</td>
</tr>
</table>

## -remarks

This method gets   an ordered list of folders. By default, this method only returns storage locations.

For best results, use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h,  for  the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.

## -see-also

<a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a>



<a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection">IObjectCollection</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-addfolder">IShellLibrary::AddFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter">LIBRARYFOLDERFILTER</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/windows/desktop/shell/sfgao">SFGAO</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>