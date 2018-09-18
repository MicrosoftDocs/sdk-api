---
UID: NF:shldisp.IAutoComplete2.SetOptions
title: IAutoComplete2::SetOptions
author: windows-sdk-content
description: Sets the current autocomplete options.
old-location: shell\IAutoComplete2_SetOptions.htm
tech.root: shell
ms.assetid: d3562845-fc28-4726-a520-29720f9924fc
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IAutoComplete2 interface [Windows Shell],SetOptions method, IAutoComplete2.SetOptions, IAutoComplete2::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IAutoComplete2 interface, _win32_IAutoComplete2_SetOptions, shell.IAutoComplete2_SetOptions, shldisp/IAutoComplete2::SetOptions
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
 - IAutoComplete2.SetOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutoComplete2::SetOptions


## -description


Sets the current autocomplete options.


## -parameters




### -param dwFlag [in]

Type: <b>DWORD</b>

One or more flags from the <a href="https://msdn.microsoft.com/e0a583da-c2bd-4757-868d-a63e697142e2">AUTOCOMPLETEOPTIONS</a> enumeration that specify autocomplete options.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The TAB key is disabled by default because it is typically used to navigate from control to control, not within a control. If you set the <a href="https://msdn.microsoft.com/e0a583da-c2bd-4757-868d-a63e697142e2">ACO_USETAB</a> flag in <i>dwFlag</i>, users can navigate to a string in the drop-down list by pressing the TAB key. If the drop-down list is closed, the TAB key allows the user to navigate from control to control, as usual. The user can close the drop-down list by pressing the ESC key.




## -see-also




<a href="https://msdn.microsoft.com/c093719f-7176-4ba4-ae75-399e8beeebf0">IAutoComplete2</a>



<a href="https://msdn.microsoft.com/00c2aa5f-eebc-479c-ac33-6efb3acb1051">IAutoComplete2::GetOptions</a>
 

 

