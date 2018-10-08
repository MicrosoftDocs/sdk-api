---
UID: NF:textserv.ITextHost2.TxGetWindowStyles
title: ITextHost2::TxGetWindowStyles
author: windows-sdk-content
description: Retrieves the window styles and extended windows styles of the text host window.
old-location: controls\itexthost2_txgetwindowstyles.htm
tech.root: controls
ms.assetid: 51885B3E-3DEE-461C-8625-3DE9D8C1F992
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetWindowStyles method, ITextHost2.TxGetWindowStyles, ITextHost2::TxGetWindowStyles, TxGetWindowStyles, TxGetWindowStyles method [Windows Controls], TxGetWindowStyles method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgetwindowstyles, textserv/ITextHost2::TxGetWindowStyles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost2.TxGetWindowStyles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost2::TxGetWindowStyles


## -description


Retrieves the window styles and extended windows styles of the text host window.


## -parameters




### -param pdwStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The window styles. For a description of the possible values, see <a href="https://msdn.microsoft.com/en-us/library/ms632600(v=VS.85).aspx">Window Styles</a>.


### -param pdwExStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The extended windows styles. For a description of the possible values, see <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">Extended Window Styles</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

