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

# opentype_feature_record structure


## -description



Contains information about a single OpenType feature to apply to a run.




## -struct-fields




### -field tagFeature


<a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a> structure containing a registered or private OpenType feature tag. For information on feature tags, see <a href="http://www.microsoft.com/typography/otspec/featuretags.htm">http://www.microsoft.com/typography/otspec/featuretags.htm</a>.


### -field lParameter

Value indicating how to apply the feature tag. Possible values are defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Feature is disabled and should not be applied.</td>
</tr>
<tr>
<td>1</td>
<td>Feature is active. If the feature offers several alternatives, select the first value.</td>
</tr>
<tr>
<td>Greater than 1</td>
<td>Feature is active. Select the alternative value at this index. Should be used only when multiple alternatives are available for a feature.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/188ad9a1-e0eb-411f-b6df-8c394d122d6f">OPENTYPE_TAG</a>



<a href="https://msdn.microsoft.com/f43a0873-f499-4d66-9fce-57f332c1dc77">TEXTRANGE_PROPERTIES</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

