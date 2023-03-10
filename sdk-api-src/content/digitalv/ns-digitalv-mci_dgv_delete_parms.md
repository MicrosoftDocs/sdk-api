---
UID: NS:digitalv.MCI_DGV_DELETE_PARMS
title: MCI_DGV_DELETE_PARMS (digitalv.h)
description: The MCI_DGV_DELETE_PARMS structure contains parameters for the MCI_DELETE command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_DELETE_PARMS","MCI_DGV_DELETE_PARMS","MCI_DGV_DELETE_PARMS structure [Windows Multimedia]","_win32_MCI_DGV_DELETE_PARMS_str","digitalv/MCI_DGV_DELETE_PARMS","multimedia.mci_dgv_delete_parms"]
old-location: multimedia\mci_dgv_delete_parms.htm
tech.root: Multimedia
ms.assetid: 0150a749-c8f3-4cc1-b212-c2a280f55afd
ms.date: 12/05/2018
ms.keywords: '*LPMCI_DGV_DELETE_PARMS, MCI_DGV_DELETE_PARMS, MCI_DGV_DELETE_PARMS structure [Windows Multimedia], _win32_MCI_DGV_DELETE_PARMS_str, digitalv/MCI_DGV_DELETE_PARMS, multimedia.mci_dgv_delete_parms'
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
req.typenames: MCI_DGV_DELETE_PARMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_DELETE_PARMS
 - digitalv/MCI_DGV_DELETE_PARMS
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
 - MCI_DGV_DELETE_PARMS
---

# MCI_DGV_DELETE_PARMS structure


## -description

The <b>MCI_DGV_DELETE_PARMS</b> structure contains parameters for the <a href="/windows/desktop/Multimedia/mci-delete">MCI_DELETE</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field dwFrom

Starting position for delete.

### -field dwTo

Ending position for delete.

### -field ptOffset

### -field ptExtent

### -field rc

Rectangle describing area to delete. <a href="/previous-versions//ms536136(v=vs.85)">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.

### -field dwAudioStream

Audio stream.

### -field dwVideoStream

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-delete">MCI_DELETE</a>



<a href="/previous-versions//ms536136(v=vs.85)">RECT</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

