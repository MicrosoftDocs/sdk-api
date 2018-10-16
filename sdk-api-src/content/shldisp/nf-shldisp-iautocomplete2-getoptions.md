---
UID: NF:shldisp.IAutoComplete2.GetOptions
title: IAutoComplete2::GetOptions
author: windows-sdk-content
description: Gets the current autocomplete options.
old-location: shell\IAutoComplete2_GetOptions.htm
tech.root: shell
ms.assetid: 00c2aa5f-eebc-479c-ac33-6efb3acb1051
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IAutoComplete2 interface, IAutoComplete2 interface [Windows Shell],GetOptions method, IAutoComplete2.GetOptions, IAutoComplete2::GetOptions, _win32_IAutoComplete2_GetOptions, shell.IAutoComplete2_GetOptions, shldisp/IAutoComplete2::GetOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
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
 - IAutoComplete2.GetOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutoComplete2::GetOptions


## -description


Gets the current autocomplete options.


## -parameters




### -param pdwFlag [out]

Type: <b>DWORD*</b>

One or more flags from the <a href="https://msdn.microsoft.com/e0a583da-c2bd-4757-868d-a63e697142e2">AUTOCOMPLETEOPTIONS</a> enumeration that indicate the options that are currently set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c093719f-7176-4ba4-ae75-399e8beeebf0">IAutoComplete2</a>



<a href="https://msdn.microsoft.com/d3562845-fc28-4726-a520-29720f9924fc">IAutoComplete2::SetOptions</a>
 

 

