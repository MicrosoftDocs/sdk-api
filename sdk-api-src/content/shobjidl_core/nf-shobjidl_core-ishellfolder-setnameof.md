---
UID: NF:shobjidl_core.IShellFolder.SetNameOf
title: IShellFolder::SetNameOf
author: windows-sdk-content
description: Sets the display name of a file object or subfolder, changing the item identifier in the process.
old-location: shell\IShellFolder_SetNameOf.htm
old-project: shell
ms.assetid: b975df89-9289-4344-9c55-f11ee83229dd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellFolder interface [Windows Shell],SetNameOf method, IShellFolder.SetNameOf, IShellFolder2 interface [Windows Shell],SetNameOf method, IShellFolder2::SetNameOf, IShellFolder::SetNameOf, SetNameOf, SetNameOf method [Windows Shell], SetNameOf method [Windows Shell],IShellFolder interface, SetNameOf method [Windows Shell],IShellFolder2 interface, _win32_IShellFolder_SetNameOf, shell.IShellFolder_SetNameOf, shobjidl_core/IShellFolder2::SetNameOf, shobjidl_core/IShellFolder::SetNameOf
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder.SetNameOf
 - IShellFolder2.SetNameOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellFolder::SetNameOf


## -description


Sets the display name of a file object or subfolder, changing the item identifier in the process.


## -parameters




### -param hwnd




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that uniquely identifies the file object or subfolder relative to the parent folder. The structure must contain exactly one <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure followed by a terminating zero.


### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that specifies the new display name.


### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDNF</a></b>

Flags that indicate the type of name specified by the <i>pszName</i> parameter. For a list of possible values and combinations of values, see <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDNF</a>.


### -param ppidlOut [out]

Type: <b>PITEMID_CHILD*</b>

Optional. If specified, the address of a pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that receives the <b>ITEMIDLIST</b> of the renamed item. The caller requests this value by passing a non-null <i>ppidlOut</i>. Implementations of <b>IShellFolder::SetNameOf</b> must return a pointer to the new <b>ITEMIDLIST</b> in the <i>ppidlOut</i> parameter.


#### - hwndOwner [in]

Type: <b>HWND</b>

A handle to the owner window of any dialog or message box that the client displays.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Changing the display name of a file system object, or a folder within it, renames the file or directory.

Before calling this method, applications should call <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a> and check that the SFGAO_CANRENAME flag is set. Note that this flag is essentially a hint to namespace clients. It does not necessarily imply that <b>IShellFolder::SetNameOf</b> will succeed or fail.

Implementers of <b>IShellFolder::SetNameOf</b> must call <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> with both the old and new absolute PIDLs once the renaming of an object is complete. This following example shows the call to <b>SHChangeNotify</b> following the renaming of a folder object. 

                


```
SHChangeNotify(SHCNE_RENAMEFOLDER, SHCNF_IDLIST, pidlFullOld, pidlFullNew);
```


This call prevents both the old and new names being displayed in the view.



