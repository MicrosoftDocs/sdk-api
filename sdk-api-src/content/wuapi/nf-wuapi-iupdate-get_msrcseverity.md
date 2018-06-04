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

# IUpdate::get_MsrcSeverity


## -description


Gets the Microsoft Security Response Center severity rating of the update.

This property is read-only.


## -parameters


## -remarks




The following ratings are the possible severity ratings of a security issue that is fixed by an update. These ratings were revised by the Microsoft Security Response Center in November 2002.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="Critical"></a><a id="critical"></a><a id="CRITICAL"></a>Critical

</td>
<td width="60%">
A security issue whose exploitation could allow the propagation of an Internet worm without user action.

</td>
</tr>
<tr>
<td width="40%">
<a id="Important"></a><a id="important"></a><a id="IMPORTANT"></a>Important

</td>
<td width="60%">
A security issue whose exploitation could result in compromise of the confidentiality, integrity, or availability of users' data, or of the integrity or availability of processing resources.

</td>
</tr>
<tr>
<td width="40%">
<a id="Moderate"></a><a id="moderate"></a><a id="MODERATE"></a>Moderate

</td>
<td width="60%">
Exploitation is mitigated to a significant degree by factors such as default configuration, auditing, or difficulty of exploitation.

</td>
</tr>
<tr>
<td width="40%">
<a id="Low"></a><a id="low"></a><a id="LOW"></a>Low

</td>
<td width="60%">
A security issue whose exploitation is extremely difficult, or whose impact is minimal.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

