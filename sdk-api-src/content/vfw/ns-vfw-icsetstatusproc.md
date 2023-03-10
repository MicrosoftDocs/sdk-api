---
UID: NS:vfw.ICSETSTATUSPROC
title: ICSETSTATUSPROC (vfw.h)
description: The ICSETSTATUSPROC structure contains status information used with the ICM_SET_STATUS_PROC message.
helpviewer_keywords: ["ICSETSTATUSPROC","ICSETSTATUSPROC structure [Windows Multimedia]","multimedia.icsetstatusproc_COLLISION563","multimedia.icsetstatusproc_struct","vfw/ICSETSTATUSPROC"]
old-location: multimedia\icsetstatusproc_struct.htm
tech.root: Multimedia
ms.assetid: 32f115a4-3096-4af0-a254-1bac39a830d7
ms.date: 12/05/2018
ms.keywords: ICSETSTATUSPROC, ICSETSTATUSPROC structure [Windows Multimedia], multimedia.icsetstatusproc_COLLISION563, multimedia.icsetstatusproc_struct, vfw/ICSETSTATUSPROC
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
targetos: Windows
req.typenames: ICSETSTATUSPROC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICSETSTATUSPROC
 - vfw/ICSETSTATUSPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICSETSTATUSPROC
---

# ICSETSTATUSPROC structure


## -description

The <b>ICSETSTATUSPROC</b> structure contains status information used with the <a href="/windows/desktop/Multimedia/icm-set-status-proc">ICM_SET_STATUS_PROC</a> message.

## -struct-fields

### -field dwFlags

Reserved; set to zero.

### -field lParam

Parameter that contains a constant to pass to the status procedure.

### -field Status

 




#### - fpfnStatus

Pointer to the status function. Specify <b>NULL</b> if status messages should not be sent. For more information about the callback function, see the <a href="/previous-versions/dd743620(v=vs.85)">MyStatusProc</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/icm-set-status-proc">ICM_SET_STATUS_PROC</a>



<a href="/previous-versions/dd743620(v=vs.85)">MyStatusProc</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

