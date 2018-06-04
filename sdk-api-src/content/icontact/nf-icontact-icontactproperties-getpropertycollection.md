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

# IContactProperties::GetPropertyCollection


## -description


Returns an <a href="https://msdn.microsoft.com/dec9430d-2174-42fe-85c1-16fa7e7adc0c">IContactPropertyCollection</a> for the current contact. 
		Optionally, filters the <b>IContactPropertyCollection</b> to enumerate only some values.


## -parameters




### -param ppPropertyCollection [out]

Type: <b><a href="https://msdn.microsoft.com/dec9430d-2174-42fe-85c1-16fa7e7adc0c">IContactPropertyCollection</a>**</b>

On success, points to the new <a href="https://msdn.microsoft.com/dec9430d-2174-42fe-85c1-16fa7e7adc0c">IContactPropertyCollection</a>.


### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT. 


### -param pszMultiValueName [in]

Type: <b>LPCWSTR</b>

Specifies the name of the collection (for example: emailAddresses or [namespace]arrayNode). 
				If <b>NULL</b>, all collections are searched for <i>ppszLabels</i>. 


### -param dwLabelCount [in]

Type: <b>DWORD</b>

Specifies the number of labels in <i>ppszLabels</i>. 
				If zero, all subproperties with labels are returned. 


### -param ppszLabels [in]

Type: <b>LPCWSTR</b>

Specifies an array of string labels to test for. 
				All labels in the array must be set to a valid string (not <b>NULL</b>). 


### -param fAnyLabelMatches [in]

Type: <b>BOOL</b>

TRUE if the presence of any label on a given property matches the property. 
				FALSE if all labels must be present to match the property. 


## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Always returns success. 

</td>
</tr>
</table>
 




## -remarks



Caller can enumerate all child properties of a top-level property with 
		an optional label filter applied. For example: all emailAddresses where label="work". On success, 
		collection has been reset to the location before the first element (if any are present). 
		Call <a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a> to begin querying data.



