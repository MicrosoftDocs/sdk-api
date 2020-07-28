---
UID: NF:vfw.MCIWndOpenInterface
title: MCIWndOpenInterface macro (vfw.h)
description: The MCIWndOpenInterface macro attaches the data stream or file associated with the specified interface to an MCIWnd window. You can use this macro or explicitly send the MCIWNDM_OPENINTERFACE message.
helpviewer_keywords: ["MCIWndOpenInterface","MCIWndOpenInterface macro [Windows Multimedia]","_win32_MCIWndOpenInterface","multimedia.mciwndopeninterface","vfw/MCIWndOpenInterface"]
old-location: multimedia\mciwndopeninterface.htm
tech.root: Multimedia
ms.assetid: ad31d945-27f8-48d5-a49b-e36f4beb5de6
ms.date: 12/05/2018
ms.keywords: MCIWndOpenInterface, MCIWndOpenInterface macro [Windows Multimedia], _win32_MCIWndOpenInterface, multimedia.mciwndopeninterface, vfw/MCIWndOpenInterface
f1_keywords:
- vfw/MCIWndOpenInterface
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vfw.h
api_name:
- MCIWndOpenInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndOpenInterface macro


## -description



The <b>MCIWndOpenInterface</b> macro attaches the data stream or file associated with the specified interface to an MCIWnd window. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-openinterface">MCIWNDM_OPENINTERFACE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param pUnk

Pointer to an IAVI interface that points to a file or a data stream in a file. 

