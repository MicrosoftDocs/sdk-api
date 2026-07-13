---
UID: NS:digitalv.MCI_DGV_COPY_PARMS
title: MCI_DGV_COPY_PARMS (digitalv.h)
description: The MCI_DGV_COPY_PARMS structure contains parameters for the MCI_COPY command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_COPY_PARMS","MCI_DGV_COPY_PARMS","MCI_DGV_COPY_PARMS structure [Windows Multimedia]","_win32_MCI_DGV_COPY_PARMS_str","digitalv/MCI_DGV_COPY_PARMS","multimedia.mci_dgv_copy_parms"]
old-location: multimedia\mci_dgv_copy_parms.htm
tech.root: Multimedia
ms.assetid: 314f1843-0457-4160-a9f0-71cffe676c8c
ms.date: 12/05/2018
ms.keywords: '*LPMCI_DGV_COPY_PARMS, MCI_DGV_COPY_PARMS, MCI_DGV_COPY_PARMS structure [Windows Multimedia], _win32_MCI_DGV_COPY_PARMS_str, digitalv/MCI_DGV_COPY_PARMS, multimedia.mci_dgv_copy_parms'
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
req.typenames: MCI_DGV_COPY_PARMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_COPY_PARMS
 - digitalv/MCI_DGV_COPY_PARMS
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
 - MCI_DGV_COPY_PARMS
---

# MCI_DGV_COPY_PARMS structure


## -description

The <b>MCI_DGV_COPY_PARMS</b> structure contains parameters for the <a href="/windows/desktop/Multimedia/mci-copy">MCI_COPY</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field dwFrom

Starting position for copy.

### -field dwTo

Ending position for copy.

### -field ptOffset

### -field ptExtent

### -field rc

Rectangle describing area to be copied.   Be aware that <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.

### -field dwAudioStream

Audio stream.

### -field dwVideoStream

Video stream.

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-copy">MCI_COPY</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

