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

# DEFCONTEXTMENU structure


## -description


Contains context menu information used by <a href="https://msdn.microsoft.com/055ff0a0-9ba7-463d-9684-3fd072b190da">SHCreateDefaultContextMenu</a>.


## -struct-fields




### -field hwnd

Type: <b>HWND</b>

A handle to the context menu. Set this member to the handle returned from <a href="https://msdn.microsoft.com/dd7e59f6-7d31-46d3-9606-0f9346ff2979">CreateMenu</a>.


### -field pcmcb

Type: <b><a href="https://msdn.microsoft.com/1a4c183b-97cf-4c9a-af5a-bcea7c2755a5">IContextMenuCB</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/1a4c183b-97cf-4c9a-af5a-bcea7c2755a5">IContextMenuCB</a> interface supported by the callback object. This value is optional and can be <b>NULL</b>.


### -field pidlFolder

Type: <b>PCIDLIST_ABSOLUTE</b>

The PIDL of the folder that contains the selected file object(s) or the folder of the context menu if no file objects are selected. This value is optional and can be <b>NULL</b>, in which case the PIDL is computed from the <b>psf</b> member.


### -field psf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface of the folder object that contains the selected file objects, or the folder that contains the context menu if no file objects are selected.


### -field cidl

Type: <b>UINT</b>

The count of items in member <b>apidl</b>.


### -field apidl

Type: <b>PCUITEMID_CHILD_ARRAY</b>

A pointer to a constant array of <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures. Each entry in the array describes a child item to which the context menu applies, for instance, a selected file the user wants to <b>Open</b>.


### -field punkAssociationInfo

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface on the object from which to load extensions. This parameter is optional and thus can be <b>NULL</b>. If this value is <b>NULL</b> and members <b>aKeys</b> and <b>cKeys</b> are also <b>NULL</b> (see Remarks),  <b>punkAssociationInfo</b> is computed from the <b>apidl</b> member and <b>cidl</b> via a request for <b>IQueryAssociations</b> through <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a>.

If <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> returns <b>E_NOTIMPL</b>, a default implementation is provided based on the <i>SFGAO_FOLDER</i> and <i>SFGAO_FILESYSTEM</i> attributes returned from <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>.


### -field cKeys

Type: <b>UINT</b>

The count of items in member <b>aKeys</b>. This value can be zero. If the value is zero, the extensions are loaded based on the object that supports interface <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> as specified by member <b>punkAssociationInfo</b>.  If the value is non-NULL, the extensions are loaded based only on member <b>aKeys</b> and not member <b>punkAssociationInfo</b>.

                    

<div class="alert"><b>Note</b>  The maximum number of keys is 16. Callers must enforce this limit as the API does not. Failing to do so can result in memory corruption.</div>
<div> </div>

### -field aKeys

Type: <b>const HKEY*</b>

A pointer to an HKEY that specifies the registry key from which to load extensions. This parameter is optional and can be <b>NULL</b>. If the value is <b>NULL</b>, the extensions are loaded based on the object that supports interface <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> as specified in <b>punkAssociationInfo</b>.


## -remarks



If the <b>aKeys</b> and <b>cKeys</b> members are valid and member <b>punkAssociationInfo</b> is also valid (not <b>NULL</b>), the system constructs the menu using the values of <b>aKeys</b> and <b>cKeys</b>, and ignores member <b>punkAssociationInfo</b> (<a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a>).

Members <b>apidl</b> and <b>cidl</b> can be used as parameters to method <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> to retrieve <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>.



