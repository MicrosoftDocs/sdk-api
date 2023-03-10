---
UID: NS:dde.DDEACK
title: DDEACK (dde.h)
description: Contains status flags that a DDE application passes to its partner as part of the WM_DDE_ACK message.
helpviewer_keywords: ["DDEACK","DDEACK structure [Data Exchange]","_win32_DDEACK_str","_win32_ddeack_str_cpp","dataxchg.ddeack","dde/DDEACK","winui._win32_ddeack_str"]
old-location: dataxchg\ddeack.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\ddeack.htm
ms.date: 12/05/2018
ms.keywords: DDEACK, DDEACK structure [Data Exchange], _win32_DDEACK_str, _win32_ddeack_str_cpp, dataxchg.ddeack, dde/DDEACK, winui._win32_ddeack_str
req.header: dde.h
req.include-header: Windows.h
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
req.typenames: DDEACK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DDEACK
 - dde/DDEACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dde.h
api_name:
 - DDEACK
---

# DDEACK structure


## -description

Contains status flags that a DDE application passes to its partner as part of the <a href="/windows/desktop/dataxchg/wm-dde-ack">WM_DDE_ACK</a> message. The flags provide details about the application's response to the messages <a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a>, <a href="/windows/desktop/dataxchg/wm-dde-poke">WM_DDE_POKE</a>, <a href="/windows/desktop/dataxchg/wm-dde-execute">WM_DDE_EXECUTE</a>, <a href="/windows/desktop/dataxchg/wm-dde-advise">WM_DDE_ADVISE</a>, <a href="/windows/desktop/dataxchg/wm-dde-unadvise">WM_DDE_UNADVISE</a>, and <a href="/windows/desktop/dataxchg/wm-dde-request">WM_DDE_REQUEST</a>.

## -struct-fields

### -field bAppReturnCode

Type: <b>unsigned short</b>

An application-defined return code.

### -field reserved

Type: <b>unsigned short</b>

Reserved.

### -field fBusy

Type: <b>unsigned short</b>

Indicates whether the application was busy and unable to respond to the partner's message at the time the message was received. A nonzero value indicates the partner was busy and unable to respond. The <b>fBusy</b> member is defined only when the <b>fAck</b> member is zero.

### -field fAck

Type: <b>unsigned short</b>

Indicates whether the application accepted the message from its partner. A nonzero value indicates the partner accepted the message.

### -field usFlags

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/wm-dde-ack">WM_DDE_ACK</a>



<a href="/windows/desktop/dataxchg/wm-dde-advise">WM_DDE_ADVISE</a>



<a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a>



<a href="/windows/desktop/dataxchg/wm-dde-execute">WM_DDE_EXECUTE</a>



<a href="/windows/desktop/dataxchg/wm-dde-poke">WM_DDE_POKE</a>



<a href="/windows/desktop/dataxchg/wm-dde-request">WM_DDE_REQUEST</a>



<a href="/windows/desktop/dataxchg/wm-dde-unadvise">WM_DDE_UNADVISE</a>

