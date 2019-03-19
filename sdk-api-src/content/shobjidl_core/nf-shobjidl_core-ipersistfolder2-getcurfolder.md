---
UID: NF:shobjidl_core.IPersistFolder2.GetCurFolder
title: IPersistFolder2::GetCurFolder (shobjidl_core.h)
author: windows-sdk-content
description: Gets the ITEMIDLIST for the folder object.
old-location: shell\IPersistFolder2_GetCurFolder.htm
tech.root: shell
ms.assetid: 6aaf6ed5-ae8e-4521-80cb-ec45af8827aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurFolder, GetCurFolder method [Windows Shell], GetCurFolder method [Windows Shell],IPersistFolder2 interface, IPersistFolder2 interface [Windows Shell],GetCurFolder method, IPersistFolder2.GetCurFolder, IPersistFolder2::GetCurFolder, _win32_IPersistFolder2_GetCurFolder, shell.IPersistFolder2_GetCurFolder, shobjidl_core/IPersistFolder2::GetCurFolder
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IPersistFolder2.GetCurFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistFolder2::GetCurFolder


## -description


Gets the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> for the folder object.


## -parameters




### -param ppidl

Type: <b>LPITEMIDLIST*</b>

The address of an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> pointer. This PIDL represents the absolute location of the folder and must be relative to the desktop. This is typically a copy of the PIDL passed to <a href="https://msdn.microsoft.com/179f13c9-7306-4ed5-935e-2620616b46c1">Initialize</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the folder object has not been initialized, this method returns S_FALSE and <i>ppidl</i> is set to <b>NULL</b>.



