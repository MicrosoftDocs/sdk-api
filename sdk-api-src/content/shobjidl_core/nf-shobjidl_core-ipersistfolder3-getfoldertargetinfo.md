---
UID: NF:shobjidl_core.IPersistFolder3.GetFolderTargetInfo
title: IPersistFolder3::GetFolderTargetInfo
author: windows-sdk-content
description: Provides the location and attributes of a folder shortcut's target folder.
old-location: shell\IPersistFolder3_GetFolderTargetInfo.htm
tech.root: shell
ms.assetid: 97a343af-0998-4718-8293-1eb4d2ac0c8a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetFolderTargetInfo, GetFolderTargetInfo method [Windows Shell], GetFolderTargetInfo method [Windows Shell],IPersistFolder3 interface, IPersistFolder3 interface [Windows Shell],GetFolderTargetInfo method, IPersistFolder3.GetFolderTargetInfo, IPersistFolder3::GetFolderTargetInfo, _win32_IPersistFolder3_GetFolderTargetInfo, shell.IPersistFolder3_GetFolderTargetInfo, shobjidl_core/IPersistFolder3::GetFolderTargetInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IPersistFolder3.GetFolderTargetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistFolder3::GetFolderTargetInfo


## -description


Provides the location and attributes of a folder shortcut's target folder.


## -parameters




### -param ppfti [out]

Type: <b><a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a> structure used to return the target folder's location and attributes.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a> structure might not be initialized by the caller. <b>GetFolderTargetInfo</b> must assign values to all members of the structure before returning it to the caller.
      



