---
UID: NF:shlobj_core.IActiveDesktop.GenerateDesktopItemHtml
title: IActiveDesktop::GenerateDesktopItemHtml
author: windows-sdk-content
description: Generates a generic HTML page containing the given desktop item.
old-location: lwef\iactivedesktop_generatedesktopitemhtml.htm
tech.root: lwef
ms.assetid: 653c9c92-4301-4960-b25e-e8e11f9d2fb8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GenerateDesktopItemHtml, GenerateDesktopItemHtml method [Legacy Windows Environment Features], GenerateDesktopItemHtml method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GenerateDesktopItemHtml method, IActiveDesktop.GenerateDesktopItemHtml, IActiveDesktop::GenerateDesktopItemHtml, _win32_IActiveDesktop_GenerateDesktopItemHtml, lwef.iactivedesktop_generatedesktopitemhtml, shell.iactivedesktop_generatedesktopitemhtml, shlobj_core/IActiveDesktop::GenerateDesktopItemHtml
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
 - IActiveDesktop.GenerateDesktopItemHtml
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::GenerateDesktopItemHtml


## -description


Generates a generic HTML page containing the given desktop item.


## -parameters




### -param pwszFileName [in]

Type: <b>PCWSTR</b>

A string value that contains the name under which to store the HTML file.


### -param pcomp [in]

Type: <b>LPCOMPONENT</b>

A pointer to the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure of the desktop item to insert in the HTML page. 


### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 

