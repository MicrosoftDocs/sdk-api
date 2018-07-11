---
UID: NF:oleidl.IOleLink.SetSourceDisplayName
title: IOleLink::SetSourceDisplayName
author: windows-sdk-content
description: Sets the display name for the link source.
old-location: com\iolelink_setsourcedisplayname.htm
old-project: com
ms.assetid: 762d021f-4bf1-4f90-bf41-065b8810de47
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IOleLink interface [COM],SetSourceDisplayName method, IOleLink.SetSourceDisplayName, IOleLink::SetSourceDisplayName, SetSourceDisplayName, SetSourceDisplayName method [COM], SetSourceDisplayName method [COM],IOleLink interface, _ole_iolelink_setsourcedisplayname, com.iolelink_setsourcedisplayname, oleidl/IOleLink::SetSourceDisplayName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink.SetSourceDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleLink::SetSourceDisplayName


## -description


Sets the display name for the link source.


## -parameters




### -param pszStatusText [in]

A pointer to the display name of the new link source. This parameter cannot be <b>NULL</b>.


## -returns



This method returns S_OK on success.

Values from <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> may also be returned here.




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application can call <b>IOleLink::SetSourceDisplayName</b> when the end user changes the source of a link or breaks a link. Note that this requires the linked object to create a moniker out of the display name. If you'd rather parse the display name into a moniker yourself, your container can call <a href="https://msdn.microsoft.com/85fe1d28-d9c6-46b4-abff-6afce9ff3cd0">IOleLink::SetSourceMoniker</a> instead of <b>IOleLink::SetSourceDisplayName</b>.

If you use the <a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="https://msdn.microsoft.com/c76723e8-e895-4ba1-9ba1-7e56a44cc5f2">IOleUILinkContainer::SetLinkSource</a> and <a href="https://msdn.microsoft.com/97099e4d-20ea-47fb-8ca8-27330f980038">IOleUILinkContainer::CancelLink</a>. Your implementation of these methods can call <b>IOleLink::SetSourceDisplayName</b>.

If your container application is immediately going to bind to a newly specified link source, you should call <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> and <a href="https://msdn.microsoft.com/85fe1d28-d9c6-46b4-abff-6afce9ff3cd0">IOleLink::SetSourceMoniker</a> instead, and then call <a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">IOleLink::BindToSource</a> using the bind context from the parsing operation. By reusing the bind context, you can avoid redundant loading of objects that might otherwise occur.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The contract for <b>IOleLink::SetSourceDisplayName</b> does not specify when the linked object will parse the display name into a moniker. The parsing can occur before <b>IOleLink::SetSourceDisplayName</b> returns, or the linked object can store the display name and parse it only when it needs to bind to the link source. Note that parsing the display name is potentially an expensive operation because it might require binding to the link source. The provided implementation of <b>IOleLink::SetSourceDisplayName</b> parses the display name and then releases the bind context used in the parse operation. This can result in running and then stopping the link source server.

If the linked object is bound to the current link source, the implementation of <b>IOleLink::SetSourceDisplayName</b> breaks the connection.

For more information on how the linked object stores and uses the moniker to the link source, see <a href="https://msdn.microsoft.com/85fe1d28-d9c6-46b4-abff-6afce9ff3cd0">IOleLink::SetSourceMoniker</a>.




## -see-also




<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/85fe1d28-d9c6-46b4-abff-6afce9ff3cd0">IOleLink::SetSourceMoniker</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

