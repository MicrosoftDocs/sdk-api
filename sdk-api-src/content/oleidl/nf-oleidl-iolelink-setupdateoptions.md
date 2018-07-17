---
UID: NF:oleidl.IOleLink.SetUpdateOptions
title: IOleLink::SetUpdateOptions
author: windows-sdk-content
description: Specifies how often a linked object should update its cached data.
old-location: com\iolelink_setupdateoptions.htm
old-project: com
ms.assetid: 310c25b5-a2f6-4ed7-8673-c53809fad32f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IOleLink interface [COM],SetUpdateOptions method, IOleLink.SetUpdateOptions, IOleLink::SetUpdateOptions, SetUpdateOptions, SetUpdateOptions method [COM], SetUpdateOptions method [COM],IOleLink interface, _ole_iolelink_setupdateoptions, com.iolelink_setupdateoptions, oleidl/IOleLink::SetUpdateOptions
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
 - IOleLink.SetUpdateOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleLink::SetUpdateOptions


## -description


Specifies how often a linked object should update its cached data.


## -parameters




### -param dwUpdateOpt [in]

Specifies how often a linked object should update its cached data. The possible values for <i>dwUpdateOpt</i> are taken from the enumeration <a href="https://msdn.microsoft.com/1945d4a2-dd1f-453e-ab7e-093f26171c84">OLEUPDATE</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied value is invalid.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application should call <b>IOleLink::SetUpdateOptions</b> when the end user changes the update option for a linked object.

The end user selects the update option for a linked object using the <b>Links</b> dialog box. If you use the <a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a> function to display this dialog box, you must implement the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface. The dialog box calls your <a href="https://msdn.microsoft.com/d2a7758d-9692-4e3c-8186-b74530299a6a">IOleUILinkContainer::SetLinkUpdateOptions</a> method to specify the update option chosen by the end user. Your implementation of this method should call the <b>IOleLink::SetUpdateOptions</b> method to pass the selected option to the linked object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The default update option is OLEUDPATE_ALWAYS. The linked object's implementation of <a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">IPersistStorage::Save</a> saves the current update option.

If OLEUDPATE_ALWAYS is specified as the update option, the linked object updates the link's caches in the following situations:

<ul>
<li>When the update option is changed from manual to automatic, if the link source is running.</li>
<li>
Whenever the linked object binds to the link source.</li>
<li>Whenever the link source is running and the linked object's <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>, <a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">IPersistStorage::Save</a>, or <a href="https://msdn.microsoft.com/26da5e16-5790-49c0-ba63-5feee49cd4c6">IAdviseSink::OnSave</a> implementations are called.</li>
</ul>
For both manual and automatic links, the linked object updates the cache whenever the container application calls <a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a> or <a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a>.




## -see-also




<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/2cb91b48-0026-4afa-80ab-16ac6fbce04d">IOleLink::GetUpdateOptions</a>



<a href="https://msdn.microsoft.com/c1da8b95-88e7-42b0-884c-5aa394cc49f4">IOleLink::Update</a>



<a href="https://msdn.microsoft.com/1743f99b-4c3b-47be-b77b-1d3378a44903">IOleObject::Update</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

