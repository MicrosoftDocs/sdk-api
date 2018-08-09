---
UID: NF:vfw.MCIWndOpenDialog
title: MCIWndOpenDialog macro
author: windows-sdk-content
description: The MCIWndOpenDialog macro opens a user-specified data file and corresponding type of MCI device, and associates them with an MCIWnd window.
old-location: multimedia\mciwndopendialog.htm
old-project: Multimedia
ms.assetid: 28110649-24a8-45c5-bf1a-b05a6476d9a5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MCIWndOpenDialog, MCIWndOpenDialog macro [Windows Multimedia], _win32_MCIWndOpenDialog, multimedia.mciwndopendialog, vfw/MCIWndOpenDialog
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndOpenDialog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndOpenDialog macro


## -description



The <b>MCIWndOpenDialog</b> macro opens a user-specified data file and corresponding type of MCI device, and associates them with an MCIWnd window. This macro displays the Open dialog box for the user to select the data file to associate with an MCI window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057">MCIWNDM_OPEN</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 

