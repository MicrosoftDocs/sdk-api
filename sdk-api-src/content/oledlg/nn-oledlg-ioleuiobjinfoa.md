---
UID: NN:oledlg.IOleUIObjInfoA
title: IOleUIObjInfoA (oledlg.h)
description: Implemented by containers and used by the container's Object Properties dialog box and by the Convert dialog box. (ANSI)
helpviewer_keywords: ["IOleUIObjInfo","IOleUIObjInfo interface [COM]","IOleUIObjInfo interface [COM]","described","IOleUIObjInfoA","IOleUIObjInfoW","_ole_IOleUIObjInfo","com.ioleuiobjinfo","oledlg/IOleUIObjInfo"]
old-location: com\ioleuiobjinfo.htm
tech.root: com
ms.assetid: 508dccb3-e98b-4f62-8bc3-98ca2b0d1349
ms.date: 12/05/2018
ms.keywords: IOleUIObjInfo, IOleUIObjInfo interface [COM], IOleUIObjInfo interface [COM],described, IOleUIObjInfoA, IOleUIObjInfoW, _ole_IOleUIObjInfo, com.ioleuiobjinfo, oledlg/IOleUIObjInfo
req.header: oledlg.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleUIObjInfoA
 - oledlg/IOleUIObjInfoA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleDlg.h
api_name:
 - IOleUIObjInfo
 - IOleUIObjInfoW
 - IOleUIObjInfoA
---

# IOleUIObjInfoA interface


## -description

Implemented by containers and used by the container's <b>Object Properties</b> dialog box and by the <b>Convert</b> dialog box. It provides information used by the <b>General</b> and <b>View</b> pages of the <b>Object Properties</b> dialog box , which display information about the object's size, location, type, and name. It also allows the object to be converted using the <b>Convert</b> dialog box. The <b>View</b> page allows the object's icon to be modified from its original form, and its display aspect to be changed (iconic versus content). Optionally, you can have your implementation of this interface allow the scale of the object to be changed.

## -inheritance

The <b>IOleUIObjInfo</b> interface inherits from <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>. <b>IOleUIObjInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines IOleUIObjInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
