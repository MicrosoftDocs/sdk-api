---
UID: NF:shobjidl_core.IShellFolder.GetDisplayNameOf
title: IShellFolder::GetDisplayNameOf
author: windows-sdk-content
description: Retrieves the display name for the specified file object or subfolder.
old-location: shell\IShellFolder_GetDisplayNameOf.htm
tech.root: shell
ms.assetid: 2164bbe6-e030-4a64-85db-9ee1cd3c136d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDisplayNameOf, GetDisplayNameOf method [Windows Shell], GetDisplayNameOf method [Windows Shell],IShellFolder interface, GetDisplayNameOf method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],GetDisplayNameOf method, IShellFolder.GetDisplayNameOf, IShellFolder2 interface [Windows Shell],GetDisplayNameOf method, IShellFolder2::GetDisplayNameOf, IShellFolder::GetDisplayNameOf, _win32_IShellFolder_GetDisplayNameOf, shell.IShellFolder_GetDisplayNameOf, shobjidl_core/IShellFolder2::GetDisplayNameOf, shobjidl_core/IShellFolder::GetDisplayNameOf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder.GetDisplayNameOf
 - IShellFolder2.GetDisplayNameOf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolder::GetDisplayNameOf


## -description


Retrieves the display name for the specified file object or subfolder.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL that uniquely identifies the file object or subfolder relative to the parent folder.


### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDNF</a></b>

Flags used to request the type of display name to return. For a list of possible values, see the <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDNF</a> enumerated type.


### -param pName [out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure in which to return the display name. The type of name returned in this structure can be the requested type, but the Shell folder might return a different type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is the caller's responsibility to free resources allocated by this function.

Normally, <i>pidl</i> can refer only to items contained by the parent folder. The PIDL must be single-level and contain exactly one <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure followed by a terminating zero. If you want to retrieve the display name of an item that is deeper than one level away from the parent folder, use <a href="https://msdn.microsoft.com/1cb283a6-3ebf-4986-9f32-5f6ab8d977ad">SHBindToParent</a> to bind with the item's immediate parent folder and then pass the item's single-level PIDL to <b>IShellFolder::GetDisplayNameOf</b>.

Also, if the <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDN_FORPARSING</a> flag is set in <i>uFlags</i> and the <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDN_INFOLDER</a> flag is not set, <i>pidl</i> can refer to an object at any level below the parent folder in the namespace hierarchy. At one time, <i>pidl</i> could be a multilevel PIDL, relative to the parent folder, and could contain multiple <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structures. However, this is no longer supported and <i>pidl</i> should now refer only to a single child item.

The simplest way to retrieve the display name from the structure pointed to by <i>pName</i> is to pass it to either <a href="https://msdn.microsoft.com/89dab3ee-e9f8-499a-97ec-6fe732315891">StrRetToBuf</a> or <a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a>. These functions take a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure and return the name. You can also examine the structure's <b>uType</b> member, and retrieve the name from the appropriate member.

The flags specified in <i>uFlags</i> are hints about the intended use of the name. They do not guarantee that <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> will return the requested form of the name. If that form is not available, a different one might be returned. In particular, there is no guarantee that the name returned by the <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDN_FORPARSING</a> flag will be successfully parsed by <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a>. There are also some combinations of flags that might cause the <b>GetDisplayNameOf</b>/<b>ParseDisplayName</b> round trip to not return the original identifier list. This occurrence is exceptional, but you should check to be sure.

<div class="alert"><b>Note</b>  The parsing name that is returned when <i>uFlags</i> has the <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDN_FORPARSING</a> flag set is not necessarily a normal text string. Virtual folders such as My Computer might return a string containing the folder object's GUID in the form "::{GUID}". Developers who implement <b>IShellFolder::GetDisplayNameOf</b> are encouraged to return parse names that are as close to the display names as possible, because the end user often needs to type or edit these names.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a>
 

 

