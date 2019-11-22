---
UID: NN:shobjidl_core.IShellLibrary
title: IShellLibrary (shobjidl_core.h)

description: Exposes methods for creating and managing libraries.
old-location: shell\IShellLibrary.htm
tech.root: shell
ms.assetid: c1ef3d22-7c88-42b0-93a2-5d1b75c327ba

ms.date: 12/05/2018
ms.keywords: IShellLibrary, IShellLibrary interface [Windows Shell], IShellLibrary interface [Windows Shell],described, _shell_IShellLibrary, shell.IShellLibrary, shobjidl_core/IShellLibrary
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IShellLibrary"
dev_langs:
 - c++
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
 - IShellLibrary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellLibrary interface


## -description


Exposes methods for creating and managing libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellLibrary</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-addfolder">AddFolder</a>
</td>
<td align="left" width="63%">
Adds a folder to the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-commit">Commit</a>
</td>
<td align="left" width="63%">
Commits library updates to an existing Library Description file.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder">GetDefaultSaveFolder</a>
</td>
<td align="left" width="63%">
Retrieves the default target folder that the library uses  for save operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getfolders">GetFolders</a>
</td>
<td align="left" width="63%">
Gets the set of child folders that are contained in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getfoldertype">GetFolderType</a>
</td>
<td align="left" width="63%">
Gets the library's folder type.      
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-geticon">GetIcon</a>
</td>
<td align="left" width="63%">
Gets the default icon for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getoptions">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the library's options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">LoadLibraryFromItem</a>
</td>
<td align="left" width="63%">
Loads the library from a specified library definition file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">LoadLibraryFromKnownFolder</a>
</td>
<td align="left" width="63%">
Loads  the  library  that is referenced by a  KNOWNFOLDERID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-removefolder">RemoveFolder</a>
</td>
<td align="left" width="63%">
Removes a folder from the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-resolvefolder">ResolveFolder</a>
</td>
<td align="left" width="63%">
Resolves the target location of a library folder, even if the folder has been moved or renamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">Save</a>
</td>
<td align="left" width="63%">
Saves the library to a new Library Description (*.library-ms) file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-saveinknownfolder">SaveInKnownFolder</a>
</td>
<td align="left" width="63%">
Saves the library to a new file in a specified known folder.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-setdefaultsavefolder">SetDefaultSaveFolder</a>
</td>
<td align="left" width="63%">
Sets the default target folder that the library will use for save operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-setfoldertype">SetFolderType</a>
</td>
<td align="left" width="63%">
Sets the library's folder type.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-seticon">SetIcon</a>
</td>
<td align="left" width="63%">
Sets the default icon for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-setoptions">SetOptions</a>
</td>
<td align="left" width="63%">
Sets the library options.

</td>
</tr>
</table> 


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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shaddfolderpathtolibrary">SHAddFolderPathToLibrary</a>
</td>
<td>Adds a folder to a library.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>
</td>
<td>Creates an <b>IShellLibrary</b> object.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object from a specified library definition file.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object for a specified <a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object for a specified path.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shremovefolderpathfromlibrary">SHRemoveFolderPathFromLibrary</a>
</td>
<td>Removes a folder from a library.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-shresolvefolderpathinlibrary">SHResolveFolderPathInLibrary</a>
</td>
<td>Attempts to resolve the target location of a library folder that has been moved or renamed.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary">SHResolveLibrary</a>
</td>
<td>Attempts to find the location of a library.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>
</td>
<td>Saves an <b>IShellLibrary</b> object to disk.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui">SHShowManageLibraryUI</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DEFAULTSAVEFOLDERTYPE</a>
</td>
<td>Specifies whether the default save location is public or private.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a>
</td>
<td>Specifies the library options.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags">LIBRARYSAVEFLAGS</a>
</td>
<td>Defines options for handling a name collision when saving a library.</td>
</tr>
</table>
 






## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd758089(v=vs.85)">Guidance for Implementing In-Process Extensions</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>
 

 

