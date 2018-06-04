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

# IPropertyPageSite::OnStatusChange


## -description


Informs the frame that the property page managed by this site has changed its state, that is, one or more property values have been changed in the page. Property pages should call this method whenever changes occur in their dialog boxes.


## -parameters




### -param dwFlags [in]

Indicates the changes that have occurred. This parameter can contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPPAGESTATUS_DIRTY"></a><a id="proppagestatus_dirty"></a><dl>
<dt><b>PROPPAGESTATUS_DIRTY</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The values in the pages have changed, so the state of the <b>Apply</b> button should be updated.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPPAGESTATUS_VALIDATE"></a><a id="proppagestatus_validate"></a><dl>
<dt><b>PROPPAGESTATUS_VALIDATE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Now is an appropriate time to apply changes.

</td>
</tr>
</table>
 


## -returns



This method can return the standard return values E_INVALIDARG and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>
 

 

