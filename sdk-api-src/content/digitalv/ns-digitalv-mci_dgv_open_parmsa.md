---
UID: NS:digitalv.MCI_DGV_OPEN_PARMSA
title: MCI_DGV_OPEN_PARMSA
author: windows-driver-content
description: The MCI_DGV_OPEN_PARMS structure contains information for the MCI_OPEN command for digital-video devices.
old-location: multimedia\mci_dgv_open_parms.htm
old-project: Multimedia
ms.assetid: 9256ab7f-1259-4c74-9766-fe3ed1c7215c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*LPMCI_DGV_OPEN_PARMSA, MCI_DGV_OPEN_PARMS, MCI_DGV_OPEN_PARMS structure [Windows Multimedia], MCI_DGV_OPEN_PARMSA, _win32_MCI_DGV_OPEN_PARMS_str, digitalv/MCI_DGV_OPEN_PARMS, multimedia.mci_dgv_open_parms"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MCI_DGV_OPEN_PARMSA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Digitalv.h
api_name:
-	MCI_DGV_OPEN_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_OPEN_PARMSA structure


## -description



The <b>MCI_DGV_OPEN_PARMS</b> structure contains information for the <a href="https://msdn.microsoft.com/e2ee92b5-b10b-4408-950e-3002fe775b25">MCI_OPEN</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field wDeviceID

Device ID returned to user.


### -field wReserved0

 


### -field lpstrDeviceType

Name or constant ID of device type.


### -field lpstrElementName

Optional device alias.


### -field lpstrAlias

Optional device alias.


### -field dwStyle

Window style.


### -field hWndParent

Handle to parent window.


### -field wReserved1

 




## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/e2ee92b5-b10b-4408-950e-3002fe775b25">MCI_OPEN</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

