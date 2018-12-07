---
UID: NF:shobjidl_core.IFileIsInUse.GetAppName
title: IFileIsInUse::GetAppName
author: windows-sdk-content
description: Retrieves the name of the application that is using the file.
old-location: shell\IFileIsInUse_GetAppName.htm
tech.root: shell
ms.assetid: 282334a9-28b4-4c3f-977e-824011efe381
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAppName, GetAppName method [Windows Shell], GetAppName method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetAppName method, IFileIsInUse.GetAppName, IFileIsInUse::GetAppName, _shell_IFileIsInUse_GetAppName, shell.IFileIsInUse_GetAppName, shobjidl_core/IFileIsInUse::GetAppName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileIsInUse.GetAppName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileIsInUse::GetAppName


## -description


Retrieves the name of the application that is using the file.


## -parameters




### -param ppszName [out]

Type: <b>LPWSTR*</b>

The address of a pointer to a buffer that, when this method returns successfully, receives the application name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This information can be passed to the user in a dialog box so that the user knows the source of the conflict and can act accordingly. For instance "File.txt is in use by Litware."



