---
UID: NN:oledlg.IOleUILinkInfoA
title: IOleUILinkInfoA (oledlg.h)
description: An extension of the IOleUILinkContainer interface. It returns the time that an object was last updated, which is link information that IOleUILinkContainer does not provide. (ANSI)
helpviewer_keywords: ["IOleUILinkInfo","IOleUILinkInfo interface [COM]","IOleUILinkInfo interface [COM]","described","IOleUILinkInfoA","IOleUILinkInfoW","_ole_IOleUILinkInfo","com.ioleuilinkinfo","oledlg/IOleUILinkInfo"]
old-location: com\ioleuilinkinfo.htm
tech.root: com
ms.assetid: aadac00b-47bb-42eb-8458-b23867f6b975
ms.date: 12/05/2018
ms.keywords: IOleUILinkInfo, IOleUILinkInfo interface [COM], IOleUILinkInfo interface [COM],described, IOleUILinkInfoA, IOleUILinkInfoW, _ole_IOleUILinkInfo, com.ioleuilinkinfo, oledlg/IOleUILinkInfo
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
 - IOleUILinkInfoA
 - oledlg/IOleUILinkInfoA
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
 - IOleUILinkInfo
 - IOleUILinkInfoA
---

# IOleUILinkInfoA interface


## -description

An extension of the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface. It returns the time that an object was last updated, which is link information that <b>IOleUILinkContainer</b> does not provide.

## -inheritance

The <b>IOleUILinkInfo</b> interface inherits from <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>. <b>IOleUILinkInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines IOleUILinkInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
