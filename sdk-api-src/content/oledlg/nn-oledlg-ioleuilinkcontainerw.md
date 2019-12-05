---
UID: NN:oledlg.IOleUILinkContainerW
title: IOleUILinkContainerW (oledlg.h)
description: Implemented by containers and used by OLE common dialog boxes. It supports these dialog boxes by providing the methods needed to manage a container's links.
old-location: com\ioleuilinkcontainer.htm
tech.root: com
ms.assetid: 7fc0aab3-7476-49ec-8a1d-3f4851f9f31c
ms.date: 12/05/2018
ms.keywords: IOleUILinkContainer, IOleUILinkContainer interface [COM], IOleUILinkContainer interface [COM],described, IOleUILinkContainerA, IOleUILinkContainerW, _ole_IOleUILinkContainer, com.ioleuilinkcontainer, oledlg/IOleUILinkContainer
ms.topic: interface
f1_keywords:
- oledlg/IOleUILinkContainer
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OleDlg.h
api_name:
- IOleUILinkContainer
- IOleUILinkContainerW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleUILinkContainerW interface


## -description


Implemented by containers and used by OLE common dialog boxes. It supports these dialog boxes by providing the methods needed to manage a container's links.

The <b>IOleUILinkContainer</b> methods enumerate the links associated with a container, and specify how they should be updated, automatically or manually. They change the source of a link and obtain information associated with a link. They also open a link's source document, update links, and break a link to the source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUILinkContainer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleUILinkContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUILinkContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-cancellink">CancelLink</a>
</td>
<td align="left" width="63%">
Disconnects the selected links.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getlinksource">GetLinkSource</a>
</td>
<td align="left" width="63%">
Retrieves information about a link that can be displayed in the <b>Links</b> dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getlinkupdateoptions">GetLinkUpdateOptions</a>
</td>
<td align="left" width="63%">
Determines the current update options for the link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">GetNextLink</a>
</td>
<td align="left" width="63%">
Enumerates the links in a container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-openlinksource">OpenLinkSource</a>
</td>
<td align="left" width="63%">
Opens the link's source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinksource">SetLinkSource</a>
</td>
<td align="left" width="63%">
Changes the source of a link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinkupdateoptions">SetLinkUpdateOptions</a>
</td>
<td align="left" width="63%">
Sets a link's update options to automatic or manual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-updatelink">UpdateLink</a>
</td>
<td align="left" width="63%">
Forces a link to connect to its source and update.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/ns-oledlg-oleuieditlinksa">OLEUIEDITLINKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-oleuichangesourcea">OleUIChangeSource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-oleuiupdatelinksa">OleUIUpdateLinks</a>
 

 

