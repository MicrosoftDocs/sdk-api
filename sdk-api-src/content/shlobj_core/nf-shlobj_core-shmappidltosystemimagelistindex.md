---
UID: NF:shlobj_core.SHMapPIDLToSystemImageListIndex
title: SHMapPIDLToSystemImageListIndex function
author: windows-sdk-content
description: SHMapPIDLToSystemImageListIndex may be altered or unavailable.
old-location: shell\SHMapPIDLToSystemImageListIndex.htm
old-project: shell
ms.assetid: 7f11049b-2481-496b-95e3-77d480f2c9df
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SHMapPIDLToSystemImageListIndex, SHMapPIDLToSystemImageListIndex function [Windows Shell], _win32_SHMapPIDLToSystemImageListIndex, shell.SHMapPIDLToSystemImageListIndex, shlobj_core/SHMapPIDLToSystemImageListIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
api_name:
 - SHMapPIDLToSystemImageListIndex
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHMapPIDLToSystemImageListIndex function


## -description


<p class="CCE_Message">[<b>SHMapPIDLToSystemImageListIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the icon index from the system image list that is associated with a folder item.


## -parameters




### -param pshf

TBD


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param piIndexSel

TBD




#### - piIndex [out, optional]

Type: <b>int*</b>

A pointer to an <b>int</b> that, when this function returns successfully, receives the index of the item's <b>open</b> icon in the system image list. If the item does not have a special <b>open</b> icon then the index of its normal icon is returned. If the <b>open</b> icon exists and cannot be obtained, then the value pointed to by <i>piIndex</i> is set to -1. This parameter can be <b>NULL</b> if the calling application is not interested in the <b>open</b> icon.


#### - psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

An <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface pointer for the folder that contains the item.


## -returns



Type: <b>int</b>

Returns the index of the item's normal icon in the system image list if successful, or -1 otherwise.



