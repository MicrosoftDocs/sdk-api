---
UID: NN:shobjidl_core.IShellLibrary
title: IShellLibrary (shobjidl_core.h)
description: Exposes methods for creating and managing libraries.
helpviewer_keywords: ["IShellLibrary","IShellLibrary interface [Windows Shell]","IShellLibrary interface [Windows Shell]","described","_shell_IShellLibrary","shell.IShellLibrary","shobjidl_core/IShellLibrary"]
old-location: shell\IShellLibrary.htm
tech.root: shell
ms.assetid: c1ef3d22-7c88-42b0-93a2-5d1b75c327ba
ms.date: 12/05/2018
ms.keywords: IShellLibrary, IShellLibrary interface [Windows Shell], IShellLibrary interface [Windows Shell],described, _shell_IShellLibrary, shell.IShellLibrary, shobjidl_core/IShellLibrary
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
 - IShellLibrary
 - shobjidl_core/IShellLibrary
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
 - IShellLibrary
---

# IShellLibrary interface


## -description

Exposes methods for creating and managing libraries.

## -inheritance

The <b>IShellLibrary</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellLibrary</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Custom implementations of <b>IShellLibrary</b> are not supported; client applications use the implementation provided by Shell32.dll.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use <b>IShellLibrary</b> to create a new library, query or update the attributes of an existing library.

<h3><a id="Library_Helper_Functions"></a><a id="library_helper_functions"></a><a id="LIBRARY_HELPER_FUNCTIONS"></a>Library Helper Functions</h3>
The following library helper functions are provided by Shobjidl.h.


<table class="clsStd">
<tr>
<th>Name</th>
<th>Summary</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a>
</td>
<td>Adds a folder to a library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>
</td>
<td>Creates an <b>IShellLibrary</b> object.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object from a specified library definition file.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object for a specified <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object for a specified path.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>
</td>
<td>Removes a folder from a library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-shresolvefolderpathinlibrary">SHResolveFolderPathInLibrary</a>
</td>
<td>Attempts to resolve the target location of a library folder that has been moved or renamed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary">SHResolveLibrary</a>
</td>
<td>Attempts to find the location of a library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>
</td>
<td>Saves an <b>IShellLibrary</b> object to disk.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui">SHShowManageLibraryUI</a>
</td>
<td>Shows the library management dialog, which enables users to manage the library folders and default save location.</td>
</tr>
</table>
 



<h3><a id="Library_Enumerations"></a><a id="library_enumerations"></a><a id="LIBRARY_ENUMERATIONS"></a>Library Enumerations</h3>
The following enumerations support libraries.


<table class="clsStd">
<tr>
<th>Name</th>
<th>Summary</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DEFAULTSAVEFOLDERTYPE</a>
</td>
<td>Specifies whether the default save location is public or private.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a>
</td>
<td>Specifies the library options.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a>
</td>
<td>Defines options for handling a name collision when saving a library.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd758089(v=vs.85)">Guidance for Implementing In-Process Extensions</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>
