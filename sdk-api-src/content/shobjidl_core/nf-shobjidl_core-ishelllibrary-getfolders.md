---
UID: NF:shobjidl_core.IShellLibrary.GetFolders
title: IShellLibrary::GetFolders
author: windows-sdk-content
description: Gets the set of child folders that are contained in the library.
old-location: shell\IShellLibrary_GetFolders.htm
tech.root: shell
ms.assetid: 19abc4f9-5123-4dd9-9606-21b52e28854b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetFolders, GetFolders method [Windows Shell], GetFolders method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetFolders method, IShellLibrary.GetFolders, IShellLibrary::GetFolders, LFF_ALLITEMS, LFF_FORCEFILESYSTEM, LFF_STORAGEITEMS, _shell_IShellLibrary_GetFolders, shell.IShellLibrary_GetFolders, shobjidl_core/IShellLibrary::GetFolders
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.GetFolders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::GetFolders


## -description


Gets the set of child folders that are contained in the library.


## -parameters




### -param lff [in]

Type: <b><a href="https://msdn.microsoft.com/8bcb8ee7-14a9-411e-978d-ddeed83d8392">LIBRARYFOLDERFILTER</a></b>

One of the following <a href="https://msdn.microsoft.com/8bcb8ee7-14a9-411e-978d-ddeed83d8392">LIBRARYFOLDERFILTER</a>   values that determines the folders to get. These flags cannot be combined.



#### LFF_FORCEFILESYSTEM (1)

Get only file-system folders. File-system folders  are  folders that have the  <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO_FILESYSTEM</a>  attribute set.



#### LFF_STORAGEITEMS (2)

Get all folders that can be bound to <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> objects.  These folders  are   folders that have the  <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO_STORAGE</a>  or  <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO_FILESYSTEM</a> attribute set.



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




<a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>



<a href="https://msdn.microsoft.com/d7665b26-5839-4b08-a099-ef25a68c65db">IObjectCollection</a>



<a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>



<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/7455998a-56a8-4fc1-882b-c0942fd35d8c">IShellLibrary::AddFolder</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/8bcb8ee7-14a9-411e-978d-ddeed83d8392">LIBRARYFOLDERFILTER</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/4cb85995-cdc8-4474-8c4d-c783ac91c759">SFGAO</a>



<a href="https://msdn.microsoft.com/308e7905-dfa1-438f-9e7e-f895517e7adb">SHAddFolderPathToLibrary</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>



<a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

