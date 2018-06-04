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

# GetRecoAttributes function


## -description



Retrieves the attributes of the recognizer.




## -parameters




### -param hrec

Handle to the recognizer.


### -param pRecoAttrs

The attributes of the recognizer. The attributes define the languages and capabilities that the recognizer supports. For more information, see the <a href="https://msdn.microsoft.com/5ebbb47f-1a11-4e97-8e45-29dbe07fe86d">RECO_ATTRS</a> structure.


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



A gesture recognizer should set the RF_OBJECT bit of the <a href="https://msdn.microsoft.com/5ebbb47f-1a11-4e97-8e45-29dbe07fe86d">RECO_ATTRS</a><b>::dwRecoCapabilityFlags</b> and should set every element in the <b>RECO_ATTRS</b><b>::awLanguageID</b> array to zero.

A gesture recognizer does not normally use a recognition guide. A gesture recognizer with no guide should clear the RF_LINED_INPUT and RF_BOXED_INPUT bits.

The <i>awcFriendlyName</i> parameter of the <a href="https://msdn.microsoft.com/5ebbb47f-1a11-4e97-8e45-29dbe07fe86d">RECO_ATTRS</a> structure may be empty (that is, having the first element set to the null character) when you use this structure as a return value from the <b>GetRecoAttributes Function</b>. Because this is not an error, the return code for <i>awcFriendlyName</i> in <b>GetRecoAttributes Function</b> will be S_OK, and the other fields will contain data.




## -see-also




<a href="https://msdn.microsoft.com/5ebbb47f-1a11-4e97-8e45-29dbe07fe86d">RECO_ATTRS Structure</a>
 

 

