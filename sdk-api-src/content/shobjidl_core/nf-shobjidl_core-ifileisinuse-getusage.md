---
UID: NF:shobjidl_core.IFileIsInUse.GetUsage
title: IFileIsInUse::GetUsage
author: windows-sdk-content
description: Gets a value that indicates how the file in use is being used.
old-location: shell\IFileIsInUse_GetUsage.htm
tech.root: shell
ms.assetid: 7baba34d-b246-4d48-9f0c-e950d33ed5cf
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetUsage, GetUsage method [Windows Shell], GetUsage method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetUsage method, IFileIsInUse.GetUsage, IFileIsInUse::GetUsage, _shell_IFileIsInUse_GetUsage, shell.IFileIsInUse_GetUsage, shobjidl_core/IFileIsInUse::GetUsage
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
 - IFileIsInUse.GetUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileIsInUse::GetUsage


## -description


Gets a value that indicates how the file in use is being used.


## -parameters




### -param pfut [out]

Type: <b><a href="https://msdn.microsoft.com/32b0e148-499a-401d-837c-8cea74cf9cac">FILE_USAGE_TYPE</a>*</b>

Pointer to a value that, when this method returns successfully, receives one of the <a href="https://msdn.microsoft.com/32b0e148-499a-401d-837c-8cea74cf9cac">FILE_USAGE_TYPE</a> values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



