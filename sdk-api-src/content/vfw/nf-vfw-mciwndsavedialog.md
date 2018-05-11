---
UID: NF:vfw.MCIWndSaveDialog
title: MCIWndSaveDialog macro
author: windows-driver-content
description: The MCIWndSaveDialog macro saves the content currently used by an MCI device. This macro displays the Save dialog box to let the user select a filename to store the content. You can use this macro or explicitly send the MCI_SAVE command.
old-location: multimedia\mciwndsavedialog.htm
old-project: Multimedia
ms.assetid: 3ab1121f-5122-424b-a1df-ceeb57751dac
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MCIWndSaveDialog, MCIWndSaveDialog macro [Windows Multimedia], _win32_MCIWndSaveDialog, multimedia.mciwndsavedialog, vfw/MCIWndSaveDialog
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
-	MCIWndSaveDialog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndSaveDialog macro


## -description



The <b>MCIWndSaveDialog</b> macro saves the content currently used by an MCI device. This macro displays the Save dialog box to let the user select a filename to store the content. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/286e6f31-cb93-443b-8191-8c363b366eae">MCI_SAVE</a> command.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 

