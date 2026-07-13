---
UID: NF:oledlg.OleUIUpdateLinksW
title: OleUIUpdateLinksW function (oledlg.h)
description: Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the Stop button or when all links are processed. (Unicode)
helpviewer_keywords: ["OleUIUpdateLinks", "OleUIUpdateLinks function [COM]", "OleUIUpdateLinksW", "_ole_OleUIUpdateLinks", "com.oleuiupdatelinks", "oledlg/OleUIUpdateLinks", "oledlg/OleUIUpdateLinksW"]
old-location: com\oleuiupdatelinks.htm
tech.root: com
ms.assetid: f280b061-45d8-484d-9fe1-ec4d85288bc6
ms.date: 12/05/2018
ms.keywords: OleUIUpdateLinks, OleUIUpdateLinks function [COM], OleUIUpdateLinksA, OleUIUpdateLinksW, _ole_OleUIUpdateLinks, com.oleuiupdatelinks, oledlg/OleUIUpdateLinks, oledlg/OleUIUpdateLinksA, oledlg/OleUIUpdateLinksW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIUpdateLinksW (Unicode) and OleUIUpdateLinksA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleUIUpdateLinksW
 - oledlg/OleUIUpdateLinksW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleDlg.dll
api_name:
 - OleUIUpdateLinks
 - OleUIUpdateLinksA
 - OleUIUpdateLinksW
---

# OleUIUpdateLinksW function


## -description

Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the <b>Stop</b> button or when all links are processed.

## -parameters

### -param lpOleUILinkCntr [in]

Pointer to the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface on the link container.

### -param hwndParent [in]

Parent window of the dialog box.

### -param lpszTitle [in]

Pointer to the title of the dialog box.

### -param cLinks [in]

Total number of links.

## -returns

Returns <b>TRUE</b> if the links were successfully updated; otherwise, <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getlinkupdateoptions">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-updatelink">IOleUILinkContainer::UpdateLink</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OleUIUpdateLinks as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
