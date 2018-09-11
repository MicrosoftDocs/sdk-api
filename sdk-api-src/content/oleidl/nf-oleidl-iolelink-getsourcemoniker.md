---
UID: NF:oleidl.IOleLink.GetSourceMoniker
title: IOleLink::GetSourceMoniker
author: windows-sdk-content
description: Retrieves the moniker identifying the link source of a linked object.
old-location: com\iolelink_getsourcemoniker.htm
tech.root: com
ms.assetid: ef447726-7aef-45c4-a522-a8de9a3e6b74
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSourceMoniker, GetSourceMoniker method [COM], GetSourceMoniker method [COM],IOleLink interface, IOleLink interface [COM],GetSourceMoniker method, IOleLink.GetSourceMoniker, IOleLink::GetSourceMoniker, _ole_iolelink_getsourcemoniker, com.iolelink_getsourcemoniker, oleidl/IOleLink::GetSourceMoniker
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
 - IOleLink.GetSourceMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleLink::GetSourceMoniker


## -description


Retrieves the moniker identifying the link source of a linked object.


## -parameters




### -param ppmk [out]

Address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> pointer variable that receives the interface pointer to an absolute moniker that identifies the link source. When successful, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on <i>ppmk</i>; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs the implementation must set <i>ppmk</i> to <b>NULL</b>.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No moniker is available.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application can call <b>IOleLink::GetSourceMoniker</b> to display the current source of a link in the <b>Links</b> dialog box. Note that this requires your container to use the <a href="https://msdn.microsoft.com/424036c9-c097-4507-b562-4a01f9199b1f">IMoniker::GetDisplayName</a> method to get the display name of the moniker. If you would rather get the display name directly, your container can call <a href="https://msdn.microsoft.com/a4c5bc82-f423-4a02-b8d4-49b38a9c0f42">IOleLink::GetSourceDisplayName</a> instead of <b>IOleLink::GetSourceMoniker</b>.

If you use the <a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="https://msdn.microsoft.com/10f1bc84-cc09-4a41-8f55-21314338f636">IOleUILinkContainer::GetLinkSource</a> to get the string it should display. Your implementation of that method can call <b>IOleLink::GetSourceMoniker</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The linked object stores both an absolute and a relative moniker for the link source. If the relative moniker is non-<b>NULL</b> and a moniker is available for the compound document, <b>IOleLink::GetSourceMoniker</b> returns the moniker created by composing the relative moniker onto the end of the compound document's moniker. Otherwise, it returns the absolute moniker or, if an error occurs, <b>NULL</b>.

The container specifies the absolute moniker when it calls one of the <a href="https://msdn.microsoft.com/ef52dc37-aa63-47f3-a04f-f9d22178690f">OleCreateLink</a> functions to create a link. The application can call <b>IOleLink::GetSourceMoniker</b> or <a href="https://msdn.microsoft.com/a4c5bc82-f423-4a02-b8d4-49b38a9c0f42">IOleLink::GetSourceDisplayName</a> to change the absolute moniker. In addition, the linked object automatically updates the monikers whenever it successfully binds to the link source, or when it is bound to the link source and it receives a rename notification through the <a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">IAdviseSink::OnRename</a> method.




## -see-also




<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/a4c5bc82-f423-4a02-b8d4-49b38a9c0f42">IOleLink::GetSourceDisplayName</a>



<a href="https://msdn.microsoft.com/ef447726-7aef-45c4-a522-a8de9a3e6b74">IOleLink::GetSourceMoniker</a>
 

 

