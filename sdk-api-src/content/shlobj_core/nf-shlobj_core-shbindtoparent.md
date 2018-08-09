---
UID: NF:shlobj_core.SHBindToParent
title: SHBindToParent function
author: windows-sdk-content
description: Takes a pointer to a fully qualified item identifier list (PIDL), and returns a specified interface pointer on the parent object.
old-location: shell\SHBindToParent.htm
old-project: shell
ms.assetid: 1cb283a6-3ebf-4986-9f32-5f6ab8d977ad
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHBindToParent, SHBindToParent function [Windows Shell], _win32_SHBindToParent, shell.SHBindToParent, shlobj_core/SHBindToParent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - Windows.Storage.Dll
api_name:
 - SHBindToParent
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHBindToParent function


## -description


Takes a pointer to a fully qualified item identifier list (PIDL), and returns a specified interface pointer on the parent object.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The item's PIDL.


### -param riid [in]

Type: <b>REFIID</b>

The <b>REFIID</b> of one of the interfaces exposed by the item's parent object.


### -param ppv [out]

Type: <b>VOID**</b>

A pointer to the interface specified by <i>riid</i>. You must release the object when you are finished.


### -param ppidlLast [out]

Type: <b>PCUITEMID_CHILD*</b>

The item's PIDL relative to the parent folder. This PIDL can be used with many of the methods supported by the parent folder's interfaces. If you set <i>ppidlLast</i> to <b>NULL</b>, the PIDL is not returned.



<div class="alert"><b>Note</b>  <b>SHBindToParent</b> does not allocate a new PIDL; it simply receives a pointer through this parameter. Therefore, you are not responsible for freeing this resource.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



