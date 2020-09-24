---
UID: NC:mmiscapi.MMIOPROC
title: MMIOPROC (mmiscapi.h)
description: The MMIOProc function is a custom input/output (I/O) procedure installed by the mmioInstallIOProc function.
helpviewer_keywords: ["MMIOProc","MMIOProc callback","MMIOProc callback function [Windows Multimedia]","_win32_MMIOProc","mmsystem/MMIOProc","multimedia.mmioproc"]
old-location: multimedia\mmioproc.htm
tech.root: Multimedia
ms.assetid: 8f7ca236-8bdf-477d-843d-d825cc606e0e
ms.date: 12/05/2018
ms.keywords: MMIOProc, MMIOProc callback, MMIOProc callback function [Windows Multimedia], _win32_MMIOProc, mmsystem/MMIOProc, multimedia.mmioproc
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MMIOPROC
 - mmiscapi/MMIOPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmsystem.h
api_name:
 - MMIOProc
---

# MMIOPROC callback function


## -description

The <b>MMIOProc</b> function is a custom input/output (I/O) procedure installed by the <a href="/previous-versions/dd757323(v=vs.85)">mmioInstallIOProc</a> function. <b>MMIOProc</b> is a placeholder for the application-defined function name. The address of this function can be specified in the callback-address parameter of <b>mmioInstallIOProc</b>.

## -parameters

### -param lpmmioinfo

Points to an <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure containing information about the open file.

The I/O procedure must maintain the <b>lDiskOffset</b> member in this structure to indicate the file offset to the next read or write location. The I/O procedure can use the <b>adwInfo</b>[] member to store state information. The I/O procedure should not modify any other members of the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure.

### -param uMsg

Specifies a message indicating the requested I/O operation. Messages that can be received include <a href="/windows/desktop/Multimedia/mmiom-open">MMIOM_OPEN</a>, <a href="/windows/desktop/Multimedia/mmiom-close">MMIOM_CLOSE</a>, <a href="/windows/desktop/Multimedia/mmiom-read">MMIOM_READ</a>, <a href="/windows/desktop/Multimedia/mmiom-seek">MMIOM_SEEK</a>, <a href="/windows/desktop/Multimedia/mmiom-write">MMIOM_WRITE</a>, and <a href="/windows/desktop/Multimedia/mmiom-writeflush">MMIOM_WRITEFLUSH</a>.

### -param lParam1

Specifies an application-defined parameter for the message.

### -param lParam2

Specifies an application-defined parameter for the message.

## -returns

The return value depends on the message specified by <i>uMsg</i>. If the I/O procedure does not recognize a message, it should return zero.

## -remarks

The four-character code specified by the <b>fccMMIOProc</b> member in the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure associated with a file identifies a file name extension for a custom storage system. When an application calls <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> with a file name such as "one.xyz+two", the I/O procedure associated with the four-character code "XYZ" is called to open the "two" element of the file "one.xyz".

The <a href="/previous-versions/dd757323(v=vs.85)">mmioInstallIOProc</a> function maintains a separate list of installed I/O procedures for each Windows-based application. Therefore, different applications can use the same I/O procedure identifier for different I/O procedures without conflict. However, installing an I/O procedure globally enables any process to use the procedure.

If an application calls <a href="/previous-versions/dd757323(v=vs.85)">mmioInstallIOProc</a> more than once to register the same I/O procedure, then it must call <b>mmioInstallIOProc</b> to remove the procedure once for each time it installed the procedure.


<a href="/previous-versions/dd757323(v=vs.85)">mmioInstallIOProc</a> will not prevent an application from installing two different I/O procedures with the same identifier, or installing an I/O procedure with one of the predefined identifiers ("DOS ", "MEM "). The most recently installed procedure takes precedence, and the most recently installed procedure is the first one to be removed.

When searching for a specified I/O procedure, local procedures are searched first, then global procedures.