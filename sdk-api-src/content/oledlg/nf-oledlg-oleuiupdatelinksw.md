---
UID: NF:oledlg.OleUIUpdateLinksW
title: OleUIUpdateLinksW function (oledlg.h)

description: Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the Stop button or when all links are processed.
old-location: com\oleuiupdatelinks.htm
tech.root: com
ms.assetid: f280b061-45d8-484d-9fe1-ec4d85288bc6

ms.date: 12/05/2018
ms.keywords: OleUIUpdateLinks, OleUIUpdateLinks function [COM], OleUIUpdateLinksA, OleUIUpdateLinksW, _ole_OleUIUpdateLinks, com.oleuiupdatelinks, oledlg/OleUIUpdateLinks, oledlg/OleUIUpdateLinksA, oledlg/OleUIUpdateLinksW
ms.topic: function
f1_keywords: 
 - "oledlg/OleUIUpdateLinks"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleUIUpdateLinksW function


## -description


Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the <b>Stop</b> button or when all links are processed.


## -parameters




### -param lpOleUILinkCntr [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface on the link container.


### -param hwndParent [in]

Parent window of the dialog box.


### -param lpszTitle [in]

Pointer to the title of the dialog box.


### -param cLinks [in]

Total number of links.


## -returns



Returns <b>TRUE</b> if the links were successfully updated; otherwise, <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getlinkupdateoptions">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-updatelink">IOleUILinkContainer::UpdateLink</a>
 

 

