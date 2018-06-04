---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOleUILinkContainerA::SetLinkSource


## -description


Changes the source of a link.


## -parameters




### -param dwLink [in]

Container-defined unique identifier for a single link. See <a href="https://msdn.microsoft.com/60246b31-3677-4424-a131-840feeca030f">IOleUILinkContainer::GetNextLink</a>.


### -param lpszDisplayName [in]

Pointer to new source string to be parsed.


### -param lenFileName [in]

Length of the leading file name portion of the <i>lpszDisplayName</i> string. If the link source is not stored in a file, then <i>lenFileName</i> should be 0. For OLE links, call <a href="https://msdn.microsoft.com/a4c5bc82-f423-4a02-b8d4-49b38a9c0f42">IOleLink::GetSourceDisplayName</a>.


### -param pchEaten [out]

Pointer to the number of characters successfully parsed in <i>lpszDisplayName</i>.


### -param fValidateSource [in]

<b>TRUE</b> if the moniker should be validated; for OLE links, <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> should be called. <b>FALSE</b> if the moniker should not be validated. If possible, the link should accept the unvalidated source, and mark itself as unavailable.


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
The supplied identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method from the <b>Change Source</b> dialog box, with <i>fValidateSource</i> initially set to <b>TRUE</b>. <b>Change Source</b> can be called directly or from the <b>Links</b> dialog box. If this call to <b>IOleUILinkContainer::SetLinkSource</b> returns an error (e.g., <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> failed because the source was unavailable), then you should display an <b>Invalid Link Source</b> message, and the user should be allowed to decide whether to fix the source. If the user chooses to fix the source, then the user should be returned to the <b>Change Source</b> dialog box with the invalid portion of the input string highlighted. If the user chooses not to fix the source, then <b>IOleUILinkContainer::SetLinkSource</b> should be called a second time with <i>fValidateSource</i> set to <b>FALSE</b>, and the user should be returned to the <b>Links</b> dialog box with the link marked <b>Unavailable</b>.




## -see-also




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>
 

 

