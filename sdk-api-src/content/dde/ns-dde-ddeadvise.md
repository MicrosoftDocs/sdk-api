---
UID: NS:dde.DDEADVISE
title: DDEADVISE (dde.h)
description: Contains flags that specify how a DDE server application should send data to a client application during an advise loop. A client passes a handle to a DDEADVISE structure to a server as part of a WM_DDE_ADVISE message.
helpviewer_keywords: ["CF_BITMAP","CF_DIB","CF_DIF","CF_ENHMETAFILE","CF_METAFILEPICT","CF_OEMTEXT","CF_PALETTE","CF_PENDATA","CF_RIFF","CF_SYLK","CF_TEXT","CF_TIFF","CF_UNICODETEXT","CF_WAVE","DDEADVISE","DDEADVISE structure [Data Exchange]","_win32_DDEADVISE_str","_win32_ddeadvise_str_cpp","dataxchg.ddeadvise","dde/DDEADVISE","winui._win32_ddeadvise_str"]
old-location: dataxchg\ddeadvise.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangestructures\ddeadvise.htm
ms.date: 12/05/2018
ms.keywords: CF_BITMAP, CF_DIB, CF_DIF, CF_ENHMETAFILE, CF_METAFILEPICT, CF_OEMTEXT, CF_PALETTE, CF_PENDATA, CF_RIFF, CF_SYLK, CF_TEXT, CF_TIFF, CF_UNICODETEXT, CF_WAVE, DDEADVISE, DDEADVISE structure [Data Exchange], _win32_DDEADVISE_str, _win32_ddeadvise_str_cpp, dataxchg.ddeadvise, dde/DDEADVISE, winui._win32_ddeadvise_str
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
req.typenames: DDEADVISE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DDEADVISE
 - dde/DDEADVISE
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
 - DDEADVISE
---

# DDEADVISE structure


## -description

Contains flags that specify how a DDE server application should send data to a client application during an advise loop. A client passes a handle to a <b>DDEADVISE</b> structure to a server as part of a <a href="/windows/desktop/dataxchg/wm-dde-advise">WM_DDE_ADVISE</a> message.

## -struct-fields

### -field reserved

Type: <b>unsigned short</b>

Reserved.

### -field fDeferUpd

Type: <b>unsigned short</b>

Indicates whether the server should defer sending updated data to the client. If this value is nonzero, the server should send a <a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a> message with a <b>NULL</b> data handle whenever the data item changes. In response, the client can post a <a href="/windows/desktop/dataxchg/wm-dde-request">WM_DDE_REQUEST</a> message to the server to get a handle to the updated data.

### -field fAckReq

Type: <b>short</b>

Indicates whether the server should set the <b>fAckReq</b> flag in the <a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a> messages it posts to the client. If this value is nonzero, the server should set the <b>fAckReq</b> bit.

### -field usFlags

### -field cfFormat

Type: <b>short</b>

The client application's preferred data format. The format must be a standard or registered clipboard format. The following standard clipboard formats can be used: 
                



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

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/wm-dde-advise">WM_DDE_ADVISE</a>



<a href="/windows/desktop/dataxchg/wm-dde-data">WM_DDE_DATA</a>



<a href="/windows/desktop/dataxchg/wm-dde-unadvise">WM_DDE_UNADVISE</a>

