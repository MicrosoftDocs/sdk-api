---
UID: NF:oleidl.IOleLink.Update
title: IOleLink::Update
author: windows-sdk-content
description: Updates the compound document's cached data for a linked object. This involves binding to the link source, if it is not already bound.
old-location: com\iolelink_update.htm
tech.root: com
ms.assetid: c1da8b95-88e7-42b0-884c-5aa394cc49f4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IOleLink interface [COM],Update method, IOleLink.Update, IOleLink::Update, Update, Update method [COM], Update method [COM],IOleLink interface, _ole_iolelink_update, com.iolelink_update, oleidl/IOleLink::Update
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
 - IOleLink.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleLink::Update


## -description


Updates the compound document's cached data for a linked object. This involves binding to the link source, if it is not already bound.


## -parameters




### -param pbc [in]

A pointer to the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on the bind context to be used in binding the link source. This parameter can be <b>NULL</b>. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the binding implementation should retrieve information about its environment. For more information, see <b>IBindCtx</b>.


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
<dt><b>CACHE_E_NOCACHE_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
The bind operation worked but no caches were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_S_SOMECACHES_NOTUPDATED</b></dt>
</dl>
</td>
<td width="60%">
The bind operation worked but not all caches were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Unable to bind to the link source.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application should call <b>Update</b> if the end user updates the cached data for a linked object.

The end user can update the cached data for a linked object by choosing the <b>Update Now</b> button in the <b>Links</b> dialog box. If you use the <a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="https://msdn.microsoft.com/fccee32a-3a6f-4ef8-9ca7-c5b664ee03cf">IOleUILinkContainer::UpdateLink</a> when the end user chooses the <b>Update Now</b> button. Your implementation of that method can call <b>Update</b>.

Your container application can also call <b>Update</b> to update a linked object, because that method â€” when called on a linked object â€” calls <b>Update</b>.

This method updates both automatic links and manual links. For manual links, calling <b>Update</b> or <b>Update</b> is the only way to update the caches. For more information on automatic and manual links, see <a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a>.

<h3><a id="Notes_on_Implementation"></a><a id="notes_on_implementation"></a><a id="NOTES_ON_IMPLEMENTATION"></a>Notes on Implementation</h3>
If <i>pbc</i> is non-<b>NULL</b>, the linked object's implementation of <b>Update</b> calls <a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">IBindCtx::RegisterObjectBound</a> to register the bound link source. This ensures that the link source remains running until the bind context is released.

The current caches are left intact if the link source cannot be bound.




## -see-also




<a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">IBindCtx::RegisterObjectBound</a>



<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a>



<a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

