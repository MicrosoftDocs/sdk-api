---
UID: NS:dde.DDEDATA
title: DDEDATA (dde.h)
description: Contains the data, and information about the data, sent as part of a WM_DDE_DATA message.
helpviewer_keywords: ["CF_BITMAP","CF_DIB","CF_DIF","CF_ENHMETAFILE","CF_METAFILEPICT","CF_OEMTEXT","CF_PALETTE","CF_PENDATA","CF_RIFF","CF_SYLK","CF_TEXT","CF_TIFF","CF_UNICODETEXT","CF_WAVE","DDEDATA","DDEDATA structure [Data Exchange]","_win32_DDEDATA_str","_win32_ddedata_str_cpp","dataxchg.ddedata","dde/DDEDATA","winui._win32_ddedata_str"]
old-location: dataxchg\ddedata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\ddedata.htm
ms.date: 12/05/2018
ms.keywords: CF_BITMAP, CF_DIB, CF_DIF, CF_ENHMETAFILE, CF_METAFILEPICT, CF_OEMTEXT, CF_PALETTE, CF_PENDATA, CF_RIFF, CF_SYLK, CF_TEXT, CF_TIFF, CF_UNICODETEXT, CF_WAVE, DDEDATA, DDEDATA structure [Data Exchange], _win32_DDEDATA_str, _win32_ddedata_str_cpp, dataxchg.ddedata, dde/DDEDATA, winui._win32_ddedata_str
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
req.typenames: DDEDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DDEDATA
 - dde/DDEDATA
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
 - DDEDATA
---

# DDEDATA structure


## -description

Contains the data, and information about the data, sent as part of a <a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a> message.

## -struct-fields

### -field unused

Type: <b>unsigned short</b>

Unused.

### -field fResponse

Type: <b>unsigned short</b>

Indicates whether the data was sent in response to a <a href="/windows/desktop/dataxchg/wm-dde-request">WM_DDE_REQUEST</a> message or a <a href="/windows/desktop/dataxchg/wm-dde-advise">WM_DDE_ADVISE</a> message. If this value is nonzero, the data was sent in response to a <b>WM_DDE_REQUEST</b> message.

### -field fRelease

Type: <b>unsigned short</b>

Indicates whether the application receiving the <a href="/windows/desktop/dataxchg/wm-dde-poke">WM_DDE_POKE</a> message should free the data. If this value is nonzero, the application should free the data.

### -field reserved

Type: <b>unsigned short</b>

Reserved.

### -field fAckReq

Type: <b>BYTE</b>

Indicates whether the application receiving the <a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a> message should acknowledge receipt of the data by sending a <a href="/windows/desktop/dataxchg/wm-dde-ack">WM_DDE_ACK</a> message. If this value is nonzero, the application should send the acknowledgment.

### -field usFlags

### -field cfFormat

Type: <b>short</b>

The format of the data. The format should be a standard or registered clipboard format. The following standard clipboard formats can be used:
                



#### CF_BITMAP (2)



#### CF_DIB (8)



#### CF_DIF (5)



#### CF_ENHMETAFILE (14)



#### CF_METAFILEPICT (3)



#### CF_OEMTEXT (7)



#### CF_PALETTE (9)



#### CF_PENDATA (10)



#### CF_RIFF (11)



#### CF_SYLK (4)



#### CF_TEXT (1)



#### CF_TIFF (6)



#### CF_WAVE (12)



#### CF_UNICODETEXT (13)

### -field Value

Type: <b>BYTE[1]</b>

Contains the data. The length and type of data depend on the <b>cfFormat</b> member.

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/wm-dde-ack">WM_DDE_ACK</a>



<a href="/windows/desktop/dataxchg/wm-dde-advise">WM_DDE_ADVISE</a>



<a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a>



<a href="/windows/desktop/dataxchg/wm-dde-poke">WM_DDE_POKE</a>



<a href="/windows/desktop/dataxchg/wm-dde-request">WM_DDE_REQUEST</a>

