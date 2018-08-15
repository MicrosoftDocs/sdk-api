---
UID: NN:shobjidl_core.IShellLibrary
title: IShellLibrary
author: windows-sdk-content
description: Exposes methods for creating and managing libraries.
old-location: shell\IShellLibrary.htm
old-project: shell
ms.assetid: c1ef3d22-7c88-42b0-93a2-5d1b75c327ba
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellLibrary, IShellLibrary interface [Windows Shell], IShellLibrary interface [Windows Shell],described, _shell_IShellLibrary, shell.IShellLibrary, shobjidl_core/IShellLibrary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLibrary interface


## -description


Exposes methods for creating and managing libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellLibrary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellLibrary</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7455998a-56a8-4fc1-882b-c0942fd35d8c">AddFolder</a>
</td>
<td align="left" width="63%">
Adds a folder to the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a340964d-ea20-4a3b-be8b-f4f4dbf624ed">Commit</a>
</td>
<td align="left" width="63%">
Commits library updates to an existing Library Description file.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bc501b1-2fc4-49ce-a16b-e254a3a40f46">GetDefaultSaveFolder</a>
</td>
<td align="left" width="63%">
Retrieves the default target folder that the library uses  for save operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19abc4f9-5123-4dd9-9606-21b52e28854b">GetFolders</a>
</td>
<td align="left" width="63%">
Gets the set of child folders that are contained in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/450ee4cc-5a09-4f14-832a-3982ec9de03b">GetFolderType</a>
</td>
<td align="left" width="63%">
Gets the library's folder type.      
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e39bd663-3f2d-4b72-9882-1313ee457844">GetIcon</a>
</td>
<td align="left" width="63%">
Gets the default icon for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a144505-e977-4db6-8266-c39c1de8a8f9">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the library's options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">LoadLibraryFromItem</a>
</td>
<td align="left" width="63%">
Loads the library from a specified library definition file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">LoadLibraryFromKnownFolder</a>
</td>
<td align="left" width="63%">
Loads  the  library  that is referenced by a  KNOWNFOLDERID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ba2c504-e96c-4b56-b2f2-196c0b74c9eb">RemoveFolder</a>
</td>
<td align="left" width="63%">
Removes a folder from the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3d867a1-7396-4fba-87ea-45b02f86d681">ResolveFolder</a>
</td>
<td align="left" width="63%">
Resolves the target location of a library folder, even if the folder has been moved or renamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">Save</a>
</td>
<td align="left" width="63%">
Saves the library to a new Library Description (*.library-ms) file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a6fa57f-808d-4893-a01c-f192355f8989">SaveInKnownFolder</a>
</td>
<td align="left" width="63%">
Saves the library to a new file in a specified known folder.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c65bd5e-22f4-450b-a1d5-75e564854b5f">SetDefaultSaveFolder</a>
</td>
<td align="left" width="63%">
Sets the default target folder that the library will use for save operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3e3f356-6ffd-46b9-b8a5-1b0c9df01abe">SetFolderType</a>
</td>
<td align="left" width="63%">
Sets the library's folder type.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d6d6bd5-14cc-432b-b712-64bac78f5df9">SetIcon</a>
</td>
<td align="left" width="63%">
Sets the default icon for the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bec0c71-3170-4ff9-aa87-4880d6ac7e32">SetOptions</a>
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
<a href="https://msdn.microsoft.com/308e7905-dfa1-438f-9e7e-f895517e7adb">SHAddFolderPathToLibrary</a>
</td>
<td>Adds a folder to a library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7e682a2e-5140-49ad-88de-ac681025aca4">SHCreateLibrary</a>
</td>
<td>Creates an <b>IShellLibrary</b> object.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object from a specified library definition file.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object for a specified <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>
</td>
<td>Creates and loads an <b>IShellLibrary</b> object for a specified path.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a>
</td>
<td>Removes a folder from a library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e9c8aacd-9abb-4640-b9ed-1fa417d4d4cc">SHResolveFolderPathInLibrary</a>
</td>
<td>Attempts to resolve the target location of a library folder that has been moved or renamed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a8730c09-f872-4bf8-9482-9dd5af31b509">SHResolveLibrary</a>
</td>
<td>Attempts to find the location of a library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>
</td>
<td>Saves an <b>IShellLibrary</b> object to disk.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1ac911bb-28d6-4cb6-a66a-1a0c8a4bd6a1">SHShowManageLibraryUI</a>
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
<a href="https://msdn.microsoft.com/51478854-03b2-4e1a-bc07-b9ca7e6cc33d">DEFAULTSAVEFOLDERTYPE</a>
</td>
<td>Specifies whether the default save location is public or private.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a>
</td>
<td>Specifies the library options.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a>
</td>
<td>Defines options for handling a name collision when saving a library.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/FE830DBF-3F18-453c-9A51-91E10559D0E8">Guidance for Implementing In-Process Extensions</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

