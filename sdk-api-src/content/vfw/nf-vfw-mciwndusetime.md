---
UID: NF:vfw.MCIWndUseTime
title: MCIWndUseTime macro
author: windows-driver-content
description: The MCIWndUseTime macro sets the time format of an MCI device to milliseconds. You can use this macro or explicitly send the MCIWNDM_SETTIMEFORMAT message.
old-location: multimedia\mciwndusetime.htm
old-project: Multimedia
ms.assetid: 604031d8-4cb6-49a8-a2c8-7b4966f9cdf4
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: MCIWndUseTime, MCIWndUseTime macro [Windows Multimedia], _win32_MCIWndUseTime, multimedia.mciwndusetime, vfw/MCIWndUseTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	MCIWndUseTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndUseTime macro


## -description



The <b>MCIWndUseTime</b> macro sets the time format of an MCI device to milliseconds. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/7de82094-6d35-44fd-88e7-ebd18a558cfd">MCIWNDM_SETTIMEFORMAT</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 

