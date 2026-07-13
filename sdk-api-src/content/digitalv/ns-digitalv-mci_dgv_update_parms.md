---
UID: NS:digitalv.MCI_DGV_UPDATE_PARMS
title: MCI_DGV_UPDATE_PARMS (digitalv.h)
description: The MCI_DGV_UPDATE_PARMS structure contains parameters for the MCI_UPDATE command.
helpviewer_keywords: ["*LPMCI_DGV_UPDATE_PARMS","MCI_DGV_UPDATE_PARMS","MCI_DGV_UPDATE_PARMS structure [Windows Multimedia]","_win32_MCI_DGV_UPDATE_PARMS_str","digitalv/MCI_DGV_UPDATE_PARMS","multimedia.mci_dgv_update_parms"]
old-location: multimedia\mci_dgv_update_parms.htm
tech.root: Multimedia
ms.assetid: 66289ff2-0e8c-4320-997c-b5078fc6db12
ms.date: 12/05/2018
ms.keywords: '*LPMCI_DGV_UPDATE_PARMS, MCI_DGV_UPDATE_PARMS, MCI_DGV_UPDATE_PARMS structure [Windows Multimedia], _win32_MCI_DGV_UPDATE_PARMS_str, digitalv/MCI_DGV_UPDATE_PARMS, multimedia.mci_dgv_update_parms'
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
targetos: Windows
req.typenames: MCI_DGV_UPDATE_PARMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_UPDATE_PARMS
 - digitalv/MCI_DGV_UPDATE_PARMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_UPDATE_PARMS
---

# MCI_DGV_UPDATE_PARMS structure


## -description

The <b>MCI_DGV_UPDATE_PARMS</b> structure contains parameters for the <a href="/windows/desktop/Multimedia/mci-update">MCI_UPDATE</a> command.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field ptOffset

### -field ptExtent

### -field rc

Rectangle containing positioning information. <a href="/previous-versions//ms536136(v=vs.85)">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.

### -field hDC

Handle to display context.

### -field wReserved0

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-update">MCI_UPDATE</a>



<a href="/previous-versions//ms536136(v=vs.85)">RECT</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

