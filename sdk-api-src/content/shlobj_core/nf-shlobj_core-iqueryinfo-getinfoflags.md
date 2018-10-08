---
UID: NF:shlobj_core.IQueryInfo.GetInfoFlags
title: IQueryInfo::GetInfoFlags
author: windows-sdk-content
description: Gets the information flags for an item. This method is not currently used.
old-location: shell\IQueryInfo_GetInfoFlags.htm
tech.root: shell
ms.assetid: 1baa47dd-b8e5-4535-b0eb-fd597241ed95
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetInfoFlags, GetInfoFlags method [Windows Shell], GetInfoFlags method [Windows Shell],IQueryInfo interface, IQueryInfo interface [Windows Shell],GetInfoFlags method, IQueryInfo.GetInfoFlags, IQueryInfo::GetInfoFlags, _win32_IQueryInfo_GetInfoFlags, shell.IQueryInfo_GetInfoFlags, shlobj_core/IQueryInfo::GetInfoFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IQueryInfo.GetInfoFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryInfo::GetInfoFlags


## -description


Gets the information flags for an item. This method is not currently used.


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

A pointer to a value that receives the flags for the item. If no flags are to be returned, this value should be set to zero.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if <i>pdwFlags</i> returns any flag values, or a COM-defined error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/7e256ed3-b3c7-4f9d-b3a0-e33c46fa2573">IQueryInfo</a>
 

 

