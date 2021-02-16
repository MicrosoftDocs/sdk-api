---
UID: NS:winbase._COMSTAT
title: COMSTAT (winbase.h)
description: Contains information about a communications device.
helpviewer_keywords: ["*LPCOMSTAT","COMSTAT","COMSTAT structure","LPCOMSTAT","LPCOMSTAT structure pointer","_COMSTAT","_win32_comstat_str","base.comstat_str","winbase/COMSTAT","winbase/LPCOMSTAT"]
old-location: base\comstat_str.htm
tech.root: base
ms.assetid: dd54d040-1244-425f-a43e-9071d679c4ec
ms.date: 12/05/2018
ms.keywords: '*LPCOMSTAT, COMSTAT, COMSTAT structure, LPCOMSTAT, LPCOMSTAT structure pointer, _COMSTAT, _win32_comstat_str, base.comstat_str, winbase/COMSTAT, winbase/LPCOMSTAT'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: COMSTAT, *LPCOMSTAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMSTAT
 - winbase/_COMSTAT
 - LPCOMSTAT
 - winbase/LPCOMSTAT
 - COMSTAT
 - winbase/COMSTAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - COMSTAT
---

# COMSTAT structure


## -description

Contains information about a communications device. This structure is filled by the 
<a href="/windows/desktop/api/winbase/nf-winbase-clearcommerror">ClearCommError</a> function.

## -struct-fields

### -field fCtsHold

If this member is <b>TRUE</b>, transmission is waiting for the CTS (clear-to-send) signal to be sent.

### -field fDsrHold

If this member is <b>TRUE</b>, transmission is waiting for the DSR (data-set-ready) signal to be sent.

### -field fRlsdHold

If this member is <b>TRUE</b>, transmission is waiting for the RLSD (receive-line-signal-detect) signal to be sent.

### -field fXoffHold

If this member is <b>TRUE</b>, transmission is waiting because the XOFF character was received.

### -field fXoffSent

If this member is <b>TRUE</b>, transmission is waiting because the XOFF character was transmitted. (Transmission halts when the XOFF character is transmitted to a system that takes the next character as XON, regardless of the actual character.)

### -field fEof

If this member is <b>TRUE</b>, the end-of-file (EOF) character has been received.

### -field fTxim

If this member is <b>TRUE</b>, there is a character queued for transmission that has come to the communications device by way of the 
<a href="/windows/desktop/api/winbase/nf-winbase-transmitcommchar">TransmitCommChar</a> function. The communications device transmits such a character ahead of other characters in the device's output buffer.

### -field fReserved

Reserved; do not use.

### -field cbInQue

The number of bytes received by the serial provider but not yet read by a 
<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> operation.

### -field cbOutQue

The number of bytes of user data remaining to be transmitted for all write operations. This value will be zero for a nonoverlapped write.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-clearcommerror">ClearCommError</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-transmitcommchar">TransmitCommChar</a>