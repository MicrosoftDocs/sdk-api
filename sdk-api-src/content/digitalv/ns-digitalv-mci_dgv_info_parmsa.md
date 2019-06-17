---
UID: NS:digitalv.__unnamed_struct_7
title: MCI_DGV_INFO_PARMSA (digitalv.h)
author: windows-sdk-content
description: The MCI_DGV_INFO_PARMS structure contains parameters for the MCI_INFO command for digital-video devices.
old-location: multimedia\mci_dgv_info_parms.htm
tech.root: Multimedia
ms.assetid: 812a2445-d7a0-4751-8af5-7c9d5e673e27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMCI_DGV_INFO_PARMSA, MCI_DGV_INFO_PARMS, MCI_DGV_INFO_PARMS structure [Windows Multimedia], MCI_DGV_INFO_PARMSA, _win32_MCI_DGV_INFO_PARMS_str, digitalv/MCI_DGV_INFO_PARMS, multimedia.mci_dgv_info_parms"
ms.topic: struct
f1_keywords: ["digitalv/MCI_DGV_INFO_PARMS"]
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
 - MCI_DGV_INFO_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_INFO_PARMSA
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_INFO_PARMSA structure


## -description



The <b>MCI_DGV_INFO_PARMS</b> structure contains parameters for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-info">MCI_INFO</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrReturn

Pointer to buffer for return string.


### -field dwRetSize

Size, in bytes, of return buffer.


### -field dwItem

Constant describing information to return.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions//dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-info">MCI_INFO</a>



<a href="https://docs.microsoft.com/previous-versions//dd757160(v=vs.85)">mciSendCommand</a>
 

 

