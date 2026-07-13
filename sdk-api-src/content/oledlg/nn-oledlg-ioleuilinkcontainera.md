---
UID: NN:oledlg.IOleUILinkContainerA
title: IOleUILinkContainerA (oledlg.h)
description: Implemented by containers and used by OLE common dialog boxes. It supports these dialog boxes by providing the methods needed to manage a container's links. (ANSI)
helpviewer_keywords: ["IOleUILinkContainer","IOleUILinkContainer interface [COM]","IOleUILinkContainer interface [COM]","described","IOleUILinkContainerA","IOleUILinkContainerW","_ole_IOleUILinkContainer","com.ioleuilinkcontainer","oledlg/IOleUILinkContainer"]
old-location: com\ioleuilinkcontainer.htm
tech.root: com
ms.assetid: 7fc0aab3-7476-49ec-8a1d-3f4851f9f31c
ms.date: 12/05/2018
ms.keywords: IOleUILinkContainer, IOleUILinkContainer interface [COM], IOleUILinkContainer interface [COM],described, IOleUILinkContainerA, IOleUILinkContainerW, _ole_IOleUILinkContainer, com.ioleuilinkcontainer, oledlg/IOleUILinkContainer
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
 - IOleUILinkContainerA
 - oledlg/IOleUILinkContainerA
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
 - IOleUILinkContainer
 - IOleUILinkContainerA
---

# IOleUILinkContainerA interface


## -description

Implemented by containers and used by OLE common dialog boxes. It supports these dialog boxes by providing the methods needed to manage a container's links.

The <b>IOleUILinkContainer</b> methods enumerate the links associated with a container, and specify how they should be updated, automatically or manually. They change the source of a link and obtain information associated with a link. They also open a link's source document, update links, and break a link to the source.

## -inheritance

The <b>IOleUILinkContainer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleUILinkContainer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuieditlinksa">OLEUIEDITLINKS</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuichangesourcea">OleUIChangeSource</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiupdatelinksa">OleUIUpdateLinks</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines IOleUILinkContainer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
