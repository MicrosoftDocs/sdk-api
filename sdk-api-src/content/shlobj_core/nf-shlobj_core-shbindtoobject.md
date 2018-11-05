---
UID: NF:shlobj_core.SHBindToObject
title: SHBindToObject function
author: windows-sdk-content
description: Retrieves and binds to a specified object by using the Shell namespace IShellFolder::BindToObject method.
old-location: shell\SHBindToObject.htm
tech.root: shell
ms.assetid: acc16097-8301-4118-8cb5-00aa2705306a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SHBindToObject, SHBindToObject function [Windows Shell], _shell_SHBindToObject, shell.SHBindToObject, shlobj_core/SHBindToObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHBindToObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHBindToObject function


## -description


Retrieves and binds to a specified object by using the Shell namespace <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a> method.


## -parameters




### -param psf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>. This parameter can be <b>NULL</b>.   If <i>psf</i> is <b>NULL</b>,  this indicates 
parameter <i>pidl</i> is relative to the desktop. In this case, <i>pidl</i> must specify an absolute <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


### -param pidl

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to a constant <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> to bind to that is relative to <i>psf</i>. If <i>psf</i> is <b>NULL</b>, this is an absolute <b>ITEMIDLIST</b> relative to the desktop folder.


### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on a bind context object to be used during this operation. If this parameter is not used, set it to <b>NULL</b>. Because support for <i>pbc</i> is optional for folder object implementations, some folders may not support the use of bind contexts.


### -param riid

Type: <b>REFIID</b>

Identifier of the interface to return.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer as specified in <i>riid</i> to the bound object. If an error occurs, contains a <b>NULL</b> pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  This is a helper function that gets the desktop object by calling <a href="https://msdn.microsoft.com/121cbd41-d512-4f33-b89c-d0dd9933df87">SHGetDesktopFolder</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a>
 

 

