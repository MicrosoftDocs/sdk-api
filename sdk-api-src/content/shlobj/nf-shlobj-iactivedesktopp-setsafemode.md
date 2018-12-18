---
UID: NF:shlobj.IActiveDesktopP.SetSafeMode
title: IActiveDesktopP::SetSafeMode
author: windows-sdk-content
description: Sets or updates the Microsoft Active Desktop to safe mode.
old-location: lwef\iactivedesktopp_setsafemode.htm
tech.root: lwef
ms.assetid: 1f88cd96-670f-4c54-9a66-2b3748b5e573
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IActiveDesktopP interface [Legacy Windows Environment Features],SetSafeMode method, IActiveDesktopP.SetSafeMode, IActiveDesktopP::SetSafeMode, SSM_SET, SSM_UPDATE, SetSafeMode, SetSafeMode method [Legacy Windows Environment Features], SetSafeMode method [Legacy Windows Environment Features],IActiveDesktopP interface, _win32_IActiveDesktopP_SetSafeMode, lwef.iactivedesktopp_setsafemode, shell.iactivedesktopp_setsafemode, shlobj/IActiveDesktopP::SetSafeMode
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktopP.SetSafeMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktopP::SetSafeMode


## -description


Sets or updates the Microsoft Active Desktop to safe mode.


## -parameters




### -param dwFlags

Type: <b>DWORD</b>

One of the following flags.



#### SSM_SET

Set to safe mode.



#### SSM_UPDATE

Update to safe mode.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/04d2e14a-374b-405d-803b-0bd6f57c077a">IActiveDesktopP</a>



<a href="https://msdn.microsoft.com/68d72b0f-f5e9-4fff-bb13-4c60d1dd7009">Using the Active Desktop Object</a>
 

 

