---
UID: NF:shimgdata.IShellImageData.RegisterAbort
title: IShellImageData::RegisterAbort
author: windows-sdk-content
description: Sets a callback abort object, optionally returning a pointer to the previous object.
old-location: shell\IShellImageData_RegisterAbort.htm
old-project: shell
ms.assetid: 21ea1f3b-3b8a-4a92-a1fb-c19f0e97a407
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellImageData interface [Windows Shell],RegisterAbort method, IShellImageData.RegisterAbort, IShellImageData::RegisterAbort, RegisterAbort, RegisterAbort method [Windows Shell], RegisterAbort method [Windows Shell],IShellImageData interface, _shell_IShellImageData_RegisterAbort, shell.IShellImageData_RegisterAbort, shimgdata/IShellImageData::RegisterAbort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shimgdata.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.RegisterAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageData::RegisterAbort


## -description


Sets a callback abort object, optionally returning a pointer to the previous object.


## -parameters




### -param pAbort [in]

Type: <b><a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>*</b>

A pointer to an abort object. If this parameter is <b>NULL</b>, an unhandled exception results.


### -param ppAbortPrev [out, optional]

Type: <b><a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>**</b>

The address of a pointer to the previous abort object. This parameter can be <b>NULL</b> if the previous object is not of interest.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise.



