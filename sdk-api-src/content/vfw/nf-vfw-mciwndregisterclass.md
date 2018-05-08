---
UID: NF:vfw.MCIWndRegisterClass
title: MCIWndRegisterClass function
author: windows-driver-content
description: The MCIWndRegisterClass function registers the MCI window class MCIWND_WINDOW_CLASS.
old-location: multimedia\mciwndregisterclass.htm
old-project: Multimedia
ms.assetid: e5b7964a-ec2b-4fef-912d-f702cb3ee05c
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: MCIWndRegisterClass, MCIWndRegisterClass function [Windows Multimedia], _win32_MCIWndRegisterClass, multimedia.mciwndregisterclass, vfw/MCIWndRegisterClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msvfw32.dll
api_name:
-	MCIWndRegisterClass
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# MCIWndRegisterClass function


## -description



The <b>MCIWndRegisterClass</b> function registers the MCI window class MCIWND_WINDOW_CLASS.




## -parameters






#### - hInstance

Handle to the device instance.


## -returns



Returns zero if successful.




## -remarks



After registering the MCI window class, use the <b>CreateWindow</b> or <b>CreateWindowEx</b> functions to create an MCIWnd window. If your application uses this function, it does not need to use the <a href="https://msdn.microsoft.com/7a4a22e1-6b04-4d46-8427-738181769f5b">MCIWndCreate</a> function.



