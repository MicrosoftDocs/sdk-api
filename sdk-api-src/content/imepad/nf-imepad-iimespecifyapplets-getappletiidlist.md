---
UID: NF:imepad.IImeSpecifyApplets.GetAppletIIDList
title: IImeSpecifyApplets::GetAppletIIDList (imepad.h)
description: Called from the IImePad interface to enumerate the IImePadApplet interfaces that are implemented.
helpviewer_keywords: ["GetAppletIIDList","GetAppletIIDList method [Internationalization for Windows Applications]","GetAppletIIDList method [Internationalization for Windows Applications]","IImeSpecifyApplets interface","IImeSpecifyApplets interface [Internationalization for Windows Applications]","GetAppletIIDList method","IImeSpecifyApplets.GetAppletIIDList","IImeSpecifyApplets::GetAppletIIDList","imepad/IImeSpecifyApplets::GetAppletIIDList","intl.iimespecifyapplets_getappletiidlist"]
old-location: intl\iimespecifyapplets_getappletiidlist.htm
tech.root: Intl
ms.assetid: 05FD7E9A-5C65-4FB7-B509-591B4B434961
ms.date: 12/05/2018
ms.keywords: GetAppletIIDList, GetAppletIIDList method [Internationalization for Windows Applications], GetAppletIIDList method [Internationalization for Windows Applications],IImeSpecifyApplets interface, IImeSpecifyApplets interface [Internationalization for Windows Applications],GetAppletIIDList method, IImeSpecifyApplets.GetAppletIIDList, IImeSpecifyApplets::GetAppletIIDList, imepad/IImeSpecifyApplets::GetAppletIIDList, intl.iimespecifyapplets_getappletiidlist
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IImeSpecifyApplets::GetAppletIIDList
 - imepad/IImeSpecifyApplets::GetAppletIIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImeSpecifyApplets.GetAppletIIDList
---

# IImeSpecifyApplets::GetAppletIIDList


## -description

Called from the <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface to enumerate the <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> interfaces that are implemented.

## -parameters

### -param refiid [in]

IID of the <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> interface. This IID is defined in Imepad.h as <b>IID_IImePadApplet</b>. This is for <b>IImePadApplet</b>'s future enhancement

### -param lpIIDList [in, out]

Pointer to a APPLETIIDLIST structure. Sets the applet's IID list and count.

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/imepad/nn-imepad-iimespecifyapplets">IImeSpecifyApplets</a>