---
UID: NF:vfw.MCIWndOpenInterface
title: MCIWndOpenInterface macro
author: windows-sdk-content
description: The MCIWndOpenInterface macro attaches the data stream or file associated with the specified interface to an MCIWnd window. You can use this macro or explicitly send the MCIWNDM_OPENINTERFACE message.
old-location: multimedia\mciwndopeninterface.htm
old-project: Multimedia
ms.assetid: ad31d945-27f8-48d5-a49b-e36f4beb5de6
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: MCIWndOpenInterface, MCIWndOpenInterface macro [Windows Multimedia], _win32_MCIWndOpenInterface, multimedia.mciwndopeninterface, vfw/MCIWndOpenInterface
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
 - MCIWndOpenInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndOpenInterface macro


## -description



The <b>MCIWndOpenInterface</b> macro attaches the data stream or file associated with the specified interface to an MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/73cbd637-d315-4b39-a978-2b72aed1f303">MCIWNDM_OPENINTERFACE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param pUnk

Pointer to an IAVI interface that points to a file or a data stream in a file. 

