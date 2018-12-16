---
UID: NF:vfw.MCIWndSave
title: MCIWndSave macro
author: windows-sdk-content
description: The MCIWndSave macro saves the content currently used by an MCI device.
old-location: multimedia\mciwndsave.htm
tech.root: Multimedia
ms.assetid: 11b67381-5177-4b55-b0a2-a633e60ae571
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MCIWndSave, MCIWndSave macro [Windows Multimedia], _win32_MCIWndSave, multimedia.mciwndsave, vfw/MCIWndSave
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
 - MCIWndSave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndSave macro


## -description



The <b>MCIWndSave</b> macro saves the content currently used by an MCI device. This macro can save the content to a specified data file or display the Save dialog box to let the user select a filename to store the content. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/286e6f31-cb93-443b-8191-8c363b366eae">MCI_SAVE</a> command.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param szFile

Null-terminated string containing the name and path of the destination file. Specify â€“1 for this parameter to display the Save dialog box. 

