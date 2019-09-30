---
UID: NF:vfw.MCIWndRegisterClass
title: MCIWndRegisterClass function (vfw.h)
author: windows-sdk-content
description: The MCIWndRegisterClass function registers the MCI window class MCIWND_WINDOW_CLASS.
old-location: multimedia\mciwndregisterclass.htm
tech.root: Multimedia
ms.assetid: e5b7964a-ec2b-4fef-912d-f702cb3ee05c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndRegisterClass, MCIWndRegisterClass function [Windows Multimedia], _win32_MCIWndRegisterClass, multimedia.mciwndregisterclass, vfw/MCIWndRegisterClass
ms.topic: function
f1_keywords: 
 - "vfw/MCIWndRegisterClass"
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - MCIWndRegisterClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



After registering the MCI window class, use the <b>CreateWindow</b> or <b>CreateWindowEx</b> functions to create an MCIWnd window. If your application uses this function, it does not need to use the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-mciwndcreatea">MCIWndCreate</a> function.



