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

# MsiGetFeatureInfoW function


## -description



			The 
<b>MsiGetFeatureInfo</b> function returns descriptive information for a feature.


## -parameters




### -param hProduct [in]

Handle to the product that owns the feature. This handle is obtained from 
<a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFeature [in]

Feature code for the feature about which information should be returned.


### -param lpAttributes [out, optional]

Pointer to a location containing one or more of the following Attribute flags. 





#### INSTALLFEATUREATTRIBUTE_FAVORLOCAL (1)



#### INSTALLFEATUREATTRIBUTE_FAVORSOURCE (2)



#### INSTALLFEATUREATTRIBUTE_FOLLOWPARENT (4)



#### INSTALLFEATUREATTRIBUTE_FAVORADVERTISE (8)



#### INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE (16)



#### INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE (32)

For more information, see  
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature Table</a>. The values that <b>MsiGetFeatureInfo</b> returns are double the values in the Attributes column of the Feature Table.


### -param lpTitleBuf [out, optional]

Pointer to a buffer to receive the localized name of the feature, which corresponds to the Title field in the <a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature Table</a>.

This parameter is optional and can be null.


### -param pcchTitleBuf [in, out, optional]

As input, the size of <i>lpTitleBuf</i>. As output, the number of characters returned in <i>lpTitleBuf</i>. On input, this is the full size of the buffer, and includes a space for a terminating null character. If the buffer that is passed in is too small, the count returned does not include the terminating null character.


### -param lpHelpBuf [out, optional]

Pointer to a buffer to receive the localized description of the feature, which corresponds to the Description field for the feature in the  <a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a>.
This parameter is optional and can be null.


### -param pcchHelpBuf [in, out, optional]

As input, the size of <i>lpHelpBuf</i>. As output, the number of characters returned in <i>lpHelpBuf</i>. On input, this is the full size of the buffer, and includes a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE (16)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FAVORADVERTISE (8)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FAVORLOCAL (1)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FAVORSOURCE (2)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FOLLOWPARENT (4)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE (32)


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The product handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function returns successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_FEATURE</b></dt>
</dl>
</td>
<td width="60%">
The feature is not known.

</td>
</tr>
</table>
 




## -remarks



The buffer sizes for the 
<b>MsiGetFeatureInfo</b> function should include an extra character for the terminating null character. If a buffer is too small, the returned string is truncated with null, and the buffer size contains the number of characters in the whole string, not including the terminating null character. For more information, see 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Product Query Functions</a>
 

 

