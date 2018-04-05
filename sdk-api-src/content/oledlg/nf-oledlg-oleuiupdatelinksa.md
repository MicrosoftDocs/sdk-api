---
UID: NF:oledlg.OleUIUpdateLinksA
title: OleUIUpdateLinksA function
author: windows-driver-content
description: Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the Stop button or when all links are processed.
old-location: com\oleuiupdatelinks.htm
old-project: com
ms.assetid: f280b061-45d8-484d-9fe1-ec4d85288bc6
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: OleUIUpdateLinks, OleUIUpdateLinks function [COM], OleUIUpdateLinksA, OleUIUpdateLinksW, _ole_OleUIUpdateLinks, com.oleuiupdatelinks, oledlg/OleUIUpdateLinks, oledlg/OleUIUpdateLinksA, oledlg/OleUIUpdateLinksW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: OLEUIPASTEFLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleDlg.dll
api_name:
-	OleUIUpdateLinks
-	OleUIUpdateLinksA
-	OleUIUpdateLinksW
product: Windows
targetos: Windows
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# OleUIUpdateLinksA function


## -description


Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the <b>Stop</b> button or when all links are processed.


## -parameters




### -param lpOleUILinkCntr [in]

Pointer to the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface on the link container.


### -param hwndParent [in]

Parent window of the dialog box.


### -param lpszTitle [in]

Pointer to the title of the dialog box.


### -param cLinks [in]

Total number of links.


## -returns



Returns <b>TRUE</b> if the links were successfully updated; otherwise, <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/136894a6-ddf6-4a47-80f5-997625362536">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="https://msdn.microsoft.com/fccee32a-3a6f-4ef8-9ca7-c5b664ee03cf">IOleUILinkContainer::UpdateLink</a>
 

 

