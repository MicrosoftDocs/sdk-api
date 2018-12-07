---
UID: NF:shlobj_core.IActiveDesktop.ApplyChanges
title: IActiveDesktop::ApplyChanges
author: windows-sdk-content
description: Applies changes to the Active Desktop and saves them in the registry.
old-location: lwef\iactivedesktop_applychanges.htm
tech.root: lwef
ms.assetid: 3bac5af5-f4a6-4822-83de-11633beef88a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AD_APPLY_ALL, AD_APPLY_BUFFERED_REFRESH, AD_APPLY_DYNAMICREFRESH, AD_APPLY_FORCE, AD_APPLY_HTMLGEN, AD_APPLY_REFRESH, AD_APPLY_SAVE, ApplyChanges, ApplyChanges method [Legacy Windows Environment Features], ApplyChanges method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],ApplyChanges method, IActiveDesktop.ApplyChanges, IActiveDesktop::ApplyChanges, _win32_IActiveDesktop_ApplyChanges, lwef.iactivedesktop_applychanges, shell.iactivedesktop_applychanges, shlobj_core/IActiveDesktop::ApplyChanges
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
 - IActiveDesktop.ApplyChanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::ApplyChanges


## -description


Applies changes to the Active Desktop and saves them in the registry.


## -parameters




### -param dwFlags

Type: <b>DWORD</b>

An unsigned long integer value that contains the changes to be applied. Can be one of the following values. 



#### AD_APPLY_ALL



#### AD_APPLY_BUFFERED_REFRESH



#### AD_APPLY_DYNAMICREFRESH



#### AD_APPLY_FORCE



#### AD_APPLY_HTMLGEN



#### AD_APPLY_REFRESH



#### AD_APPLY_SAVE


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

