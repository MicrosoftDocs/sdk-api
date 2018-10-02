---
UID: NF:oledlg.IOleUILinkContainerA.GetLinkUpdateOptions
title: IOleUILinkContainerA::GetLinkUpdateOptions
author: windows-sdk-content
description: Determines the current update options for a link.
old-location: com\ioleuilinkcontainer_getlinkupdateoptions.htm
tech.root: com
ms.assetid: 136894a6-ddf6-4a47-80f5-997625362536
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetLinkUpdateOptions, GetLinkUpdateOptions method [COM], GetLinkUpdateOptions method [COM],IOleUILinkContainer interface, GetLinkUpdateOptions method [COM],IOleUILinkContainerA interface, GetLinkUpdateOptions method [COM],IOleUILinkContainerW interface, IOleUILinkContainer interface [COM],GetLinkUpdateOptions method, IOleUILinkContainer::GetLinkUpdateOptions, IOleUILinkContainerA interface [COM],GetLinkUpdateOptions method, IOleUILinkContainerA.GetLinkUpdateOptions, IOleUILinkContainerA::GetLinkUpdateOptions, IOleUILinkContainerW interface [COM],GetLinkUpdateOptions method, IOleUILinkContainerW::GetLinkUpdateOptions, _ole_IOleUILinkContainer_GetLinkUpdateOptions, com.ioleuilinkcontainer_getlinkupdateoptions, oledlg/IOleUILinkContainer::GetLinkUpdateOptions, oledlg/IOleUILinkContainerA::GetLinkUpdateOptions, oledlg/IOleUILinkContainerW::GetLinkUpdateOptions
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
 - IOleUILinkContainer.GetLinkUpdateOptions
 - IOleUILinkContainerA.GetLinkUpdateOptions
 - IOleUILinkContainerW.GetLinkUpdateOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUILinkContainerA::GetLinkUpdateOptions


## -description


Determines the current update options for a link.


## -parameters




### -param dwLink [in]

Container-defined unique identifier for a single link. See <a href="https://msdn.microsoft.com/60246b31-3677-4424-a131-840feeca030f">IOleUILinkContainer::GetNextLink</a>.


### -param lpdwUpdateOpt [out]

A pointer to the location that the current update options will be written.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Insufficient access permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Containers can implement this method for OLE links simply by calling <a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a> on the link object.




## -see-also




<a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">IOleLink::SetUpdateOptions</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/60246b31-3677-4424-a131-840feeca030f">IOleUILinkContainer::GetNextLink</a>



<a href="https://msdn.microsoft.com/d2a7758d-9692-4e3c-8186-b74530299a6a">IOleUILinkContainer::SetLinkUpdateOptions</a>
 

 

