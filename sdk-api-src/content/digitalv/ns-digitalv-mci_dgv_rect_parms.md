---
UID: NS:digitalv.__unnamed_struct_0
title: MCI_DGV_RECT_PARMS (digitalv.h)
author: windows-sdk-content
description: The MCI_DGV_RECT_PARMS structure contains parameters for the MCI_FREEZE, MCI_PUT, MCI_UNFREEZE, and MCI_WHERE commands for digital-video devices.
old-location: multimedia\mci_dgv_rect_parms.htm
tech.root: Multimedia
ms.assetid: b73e6344-f5d8-4d21-bda9-ac076bf79dc8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMCI_DGV_FREEZE_PARMS, *LPMCI_DGV_PUT_PARMS, *LPMCI_DGV_RECT_PARMS, *LPMCI_DGV_UNFREEZE_PARMS, *LPMCI_DGV_WHERE_PARMS, MCI_DGV_FREEZE_PARMS, MCI_DGV_PUT_PARMS, MCI_DGV_RECT_PARMS, MCI_DGV_RECT_PARMS structure [Windows Multimedia], MCI_DGV_UNFREEZE_PARMS, MCI_DGV_WHERE_PARMS, _win32_MCI_DGV_RECT_PARMS_str, digitalv/MCI_DGV_RECT_PARMS, multimedia.mci_dgv_rect_parms"
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
 - MCI_DGV_RECT_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_RECT_PARMS
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_RECT_PARMS structure


## -description



The <b>MCI_DGV_RECT_PARMS</b> structure contains parameters for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-freeze">MCI_FREEZE</a>, <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-put">MCI_PUT</a>, <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-unfreeze">MCI_UNFREEZE</a>, and <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-where">MCI_WHERE</a> commands for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle containing positioning information. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/digitalv/ns-digitalv-mci_dgv_rect_parms">MCI_DGV_FREEZE_PARMS</a>, <a href="https://docs.microsoft.com/previous-versions//dd743397(v=vs.85)">MCI_DGV_PUT_PARMS</a>, <b>MCI_DGV_UNFREEZE_PARMS</b> and <b>MCI_DGV_WHERE_PARMS</b> structures are identical to the <b>MCI_DGV_RECT_PARMS</b> structure.

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions//dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-freeze">MCI_FREEZE</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-put">MCI_PUT</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-unfreeze">MCI_UNFREEZE</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-where">MCI_WHERE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://docs.microsoft.com/previous-versions//dd757160(v=vs.85)">mciSendCommand</a>
 

 

