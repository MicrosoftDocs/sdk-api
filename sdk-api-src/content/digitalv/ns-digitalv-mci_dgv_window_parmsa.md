---
UID: NS:digitalv.MCI_DGV_WINDOW_PARMSA
title: MCI_DGV_WINDOW_PARMSA
author: windows-sdk-content
description: The MCI_DGV_WINDOW_PARMS structure contains parameters for MCI_WINDOW command for digital-video devices.
old-location: multimedia\mci_dgv_window_parms.htm
tech.root: Multimedia
ms.assetid: 89c16949-4501-4ca0-87b6-c5f2524879a7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*LPMCI_DGV_WINDOW_PARMSA, MCI_DGV_WINDOW_PARMS, MCI_DGV_WINDOW_PARMS structure [Windows Multimedia], MCI_DGV_WINDOW_PARMSA, _win32_MCI_DGV_WINDOW_PARMS_str, digitalv/MCI_DGV_WINDOW_PARMS, multimedia.mci_dgv_window_parms"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: digitalv.h
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
 - Digitalv.h
api_name:
 - MCI_DGV_WINDOW_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_WINDOW_PARMSA
req.redist: 
---

# MCI_DGV_WINDOW_PARMSA structure


## -description



The <b>MCI_DGV_WINDOW_PARMS</b> structure contains parameters for <a href="https://msdn.microsoft.com/8b6c4d9a-ee72-4c64-aebe-6c8153167496">MCI_WINDOW</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field hWnd

Handle to the display window. If this member is MCI_DGV_WINDOW_HWND, the system uses a default window.


### -field wReserved1

 


### -field nCmdShow

Window-display command.


### -field wReserved2

 


### -field lpstrText

Window caption.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/8b6c4d9a-ee72-4c64-aebe-6c8153167496">MCI_WINDOW</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

