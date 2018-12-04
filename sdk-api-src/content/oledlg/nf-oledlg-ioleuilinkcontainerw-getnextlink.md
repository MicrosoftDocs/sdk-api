---
UID: NF:oledlg.IOleUILinkContainerW.GetNextLink
title: IOleUILinkContainerW::GetNextLink
author: windows-sdk-content
description: Enumerates the links in a container.
old-location: com\ioleuilinkcontainer_getnextlink.htm
tech.root: com
ms.assetid: 60246b31-3677-4424-a131-840feeca030f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetNextLink, GetNextLink method [COM], GetNextLink method [COM],IOleUILinkContainer interface, GetNextLink method [COM],IOleUILinkContainerA interface, GetNextLink method [COM],IOleUILinkContainerW interface, IOleUILinkContainer interface [COM],GetNextLink method, IOleUILinkContainer::GetNextLink, IOleUILinkContainerA interface [COM],GetNextLink method, IOleUILinkContainerA::GetNextLink, IOleUILinkContainerW interface [COM],GetNextLink method, IOleUILinkContainerW.GetNextLink, IOleUILinkContainerW::GetNextLink, _ole_IOleUILinkContainer_GetNextLink, com.ioleuilinkcontainer_getnextlink, oledlg/IOleUILinkContainer::GetNextLink, oledlg/IOleUILinkContainerA::GetNextLink, oledlg/IOleUILinkContainerW::GetNextLink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IOleUILinkContainer.GetNextLink
 - IOleUILinkContainerA.GetNextLink
 - IOleUILinkContainerW.GetNextLink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUILinkContainerW::GetNextLink


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




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/136894a6-ddf6-4a47-80f5-997625362536">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="https://msdn.microsoft.com/d2a7758d-9692-4e3c-8186-b74530299a6a">IOleUILinkContainer::SetLinkUpdateOptions</a>
 

 

