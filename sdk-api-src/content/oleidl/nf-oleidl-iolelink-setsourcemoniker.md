---
UID: NF:oleidl.IOleLink.SetSourceMoniker
title: IOleLink::SetSourceMoniker
author: windows-sdk-content
description: Sets the moniker for the link source.
old-location: com\iolelink_setsourcemoniker.htm
tech.root: com
ms.assetid: 85fe1d28-d9c6-46b4-abff-6afce9ff3cd0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOleLink interface [COM],SetSourceMoniker method, IOleLink.SetSourceMoniker, IOleLink::SetSourceMoniker, SetSourceMoniker, SetSourceMoniker method [COM], SetSourceMoniker method [COM],IOleLink interface, _ole_iolelink_setsourcemoniker, com.iolelink_setsourcemoniker, oleidl/IOleLink::SetSourceMoniker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleLink.SetSourceMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleLink::SetSourceMoniker


## -description


Sets the moniker for the link source.


## -parameters




### -param pmk [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on a moniker that identifies the new link source of the linked object. A value of <b>NULL</b> breaks the link.


### -param rclsid [in]

The CLSID of the link source that the linked object should use to access information about the linked object when it is not bound.


## -returns



This method returns S_OK on success.




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application can call <b>IOleLink::SetSourceMoniker</b> when the end user changes the source of a link or breaks a link. Note that this requires your container to use the <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> function to create a moniker out of the display name that the end user enters. If you'd rather have the linked object perform the parsing, your container can call <a href="https://msdn.microsoft.com/762d021f-4bf1-4f90-bf41-065b8810de47">IOleLink::SetSourceDisplayName</a> instead of <b>IOleLink::SetSourceMoniker</b>.

The end user changes the source of a link or breaks a link using the <b>Links</b> dialog box. If you use the <a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="https://msdn.microsoft.com/c76723e8-e895-4ba1-9ba1-7e56a44cc5f2">IOleUILinkContainer::SetLinkSource</a> and <a href="https://msdn.microsoft.com/97099e4d-20ea-47fb-8ca8-27330f980038">IOleUILinkContainer::CancelLink</a>; your implementation of these methods can call <b>IOleLink::SetSourceMoniker</b>.

If the linked object is currently bound to its link source, the linked object's implementation of <b>IOleLink::SetSourceMoniker</b> closes the link before changing the moniker.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a> contract does not specify how the linked object stores or uses the link source moniker. The provided implementation stores the absolute moniker specified when the link is created or when the moniker is changed; it then computes and stores a relative moniker. Future implementations might manage monikers differently to provide better moniker tracking. The absolute moniker provides the complete path to the link source. The linked object uses this absolute moniker and the moniker of the compound document to compute a relative moniker that identifies the link source relative to the compound document that contains the link.

pmkCompoundDoc-&gt;RelativePathTo(pmkAbsolute, ppmkRelative)

When binding to the link source, the linked object first tries to bind using the relative moniker. If that fails, it tries to bind the absolute moniker.

When the linked object successfully binds using either the relative or the absolute moniker, it automatically updates the other moniker. The linked object also updates both monikers when it is bound to the link source and it receives a rename notification through the <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a> method. A container application can also use the <a href="https://msdn.microsoft.com/762d021f-4bf1-4f90-bf41-065b8810de47">IOleLink::SetSourceDisplayName</a> method to change a link's moniker.

The linked object's implementation of <a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">IPersistStorage::Save</a> saves both the relative and the absolute moniker.




## -see-also




<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/ef447726-7aef-45c4-a522-a8de9a3e6b74">IOleLink::GetSourceMoniker</a>



<a href="https://msdn.microsoft.com/762d021f-4bf1-4f90-bf41-065b8810de47">IOleLink::SetSourceDisplayName</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

