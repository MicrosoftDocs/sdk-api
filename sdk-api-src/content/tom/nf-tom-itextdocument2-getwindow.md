---
UID: NF:tom.ITextDocument2.GetWindow
title: ITextDocument2::GetWindow
author: windows-sdk-content
description: Gets the handle of the window that the Text Object Model (TOM) engine is using to display output.
old-location: controls\itextdocument2_getwindow.htm
tech.root: controls
ms.assetid: 4bf5e644-292e-4847-8dad-71e8ccf86205
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetWindow, GetWindow method [Windows Controls], GetWindow method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetWindow method, ITextDocument2.GetWindow, ITextDocument2::GetWindow, controls.itextdocument2_getwindow, tom/ITextDocument2::GetWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
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
 - ITextDocument2.GetWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetWindow


## -description


Gets the handle of the window that the Text Object Model (TOM) engine is using to display output.


## -parameters




### -param pHwnd [out, retval]

Type: <b>__int64*</b>

The handle of the window that the TOM engine is using. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



A rich edit control doesn't need to own the window that the TOM engine is using. For example, the rich edit control might be windowless. 

The Input Method Editor (IME) needs the handle of the window that is receiving keyboard messages. This method retrieves that handle.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

