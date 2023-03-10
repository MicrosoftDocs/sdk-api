---
UID: NF:oledlg.IOleUILinkContainerA.GetNextLink
title: IOleUILinkContainerA::GetNextLink (oledlg.h)
description: Enumerates the links in a container. (ANSI)
helpviewer_keywords: ["GetNextLink","GetNextLink method [COM]","GetNextLink method [COM]","IOleUILinkContainer interface","GetNextLink method [COM]","IOleUILinkContainerA interface","GetNextLink method [COM]","IOleUILinkContainerW interface","IOleUILinkContainer interface [COM]","GetNextLink method","IOleUILinkContainer::GetNextLink","IOleUILinkContainerA interface [COM]","GetNextLink method","IOleUILinkContainerA.GetNextLink","IOleUILinkContainerA::GetNextLink","IOleUILinkContainerW interface [COM]","GetNextLink method","IOleUILinkContainerW::GetNextLink","_ole_IOleUILinkContainer_GetNextLink","com.ioleuilinkcontainer_getnextlink","oledlg/IOleUILinkContainer::GetNextLink","oledlg/IOleUILinkContainerA::GetNextLink","oledlg/IOleUILinkContainerW::GetNextLink"]
old-location: com\ioleuilinkcontainer_getnextlink.htm
tech.root: com
ms.assetid: 60246b31-3677-4424-a131-840feeca030f
ms.date: 12/05/2018
ms.keywords: GetNextLink, GetNextLink method [COM], GetNextLink method [COM],IOleUILinkContainer interface, GetNextLink method [COM],IOleUILinkContainerA interface, GetNextLink method [COM],IOleUILinkContainerW interface, IOleUILinkContainer interface [COM],GetNextLink method, IOleUILinkContainer::GetNextLink, IOleUILinkContainerA interface [COM],GetNextLink method, IOleUILinkContainerA.GetNextLink, IOleUILinkContainerA::GetNextLink, IOleUILinkContainerW interface [COM],GetNextLink method, IOleUILinkContainerW::GetNextLink, _ole_IOleUILinkContainer_GetNextLink, com.ioleuilinkcontainer_getnextlink, oledlg/IOleUILinkContainer::GetNextLink, oledlg/IOleUILinkContainerA::GetNextLink, oledlg/IOleUILinkContainerW::GetNextLink
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
 - IOleUILinkContainerA::GetNextLink
 - oledlg/IOleUILinkContainerA::GetNextLink
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
 - IOleUILinkContainer.GetNextLink
 - IOleUILinkContainerA.GetNextLink
 - IOleUILinkContainerW.GetNextLink
---

# IOleUILinkContainerA::GetNextLink


## -description

Enumerates the links in a container.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. This value is only passed to other methods on this interface, so it can be any value that uniquely identifies a link to the container. Containers frequently use the pointer to the link's container site object for this value.

## -returns

Returns a container's link identifiers in sequence; <b>NULL</b> if it has returned the last link.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method to enumerate the links in a container. If the value passed in <i>dwLink</i> is <b>NULL</b>, then the container should return the first link's identifier. If <i>dwLink</i> identifies the last link in the container, then the container should return <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getlinkupdateoptions">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinkupdateoptions">IOleUILinkContainer::SetLinkUpdateOptions</a>
