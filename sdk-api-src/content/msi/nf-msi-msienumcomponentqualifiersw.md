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

# MsiEnumComponentQualifiersW function


## -description


The 
<b>MsiEnumComponentQualifiers</b> function enumerates the advertised qualifiers for the given component. This function retrieves one qualifier each time it is called.


## -parameters




### -param szComponent [in]

Specifies component whose qualifiers are to be enumerated.


### -param iIndex [in]

Specifies the index of the qualifier to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumComponentQualifiers</b> function and then incremented for subsequent calls. Because qualifiers are not ordered, any new qualifier has an arbitrary index. This means that the function can return qualifiers in any order.


### -param lpQualifierBuf [out]

Pointer to a buffer that receives the qualifier code.


### -param pcchQualifierBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpQualifierBuf</i> parameter. On input, this size should include the terminating null character. On return, the value does not include the null character.


### -param lpApplicationDataBuf [out]

Pointer to a buffer that receives the application registered data for the qualifier. This parameter can be null.


### -param pcchApplicationDataBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpApplicationDataBuf</i> parameter. On input, this size should include the terminating null character. On return, the value does not include the null character. This parameter can be null only if the <i>lpApplicationDataBuf </i>parameter is null.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is to small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no qualifiers to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The specified component is unknown.

</td>
</tr>
</table>
 




## -remarks



To enumerate qualifiers, an application should initially call the 
<b>MsiEnumComponentQualifiers</b> function with the<i> iIndex </i>parameter set to zero. The application should then increment the <i> iIndex </i> parameter and call 
<b>MsiEnumComponentQualifiers</b> until there are no more qualifiers (that is, until the function returns ERROR_NO_MORE_ITEMS).

When 
<b>MsiEnumComponentQualifiers</b> returns, the <i>pcchQualifierBuf</i> parameter contains the length of the qualifier string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not big enough, 
<b>MsiEnumComponentQualifiers</b> returns ERROR_MORE_DATA, and this parameter contains the size of the string, in characters, without counting the null character. The same mechanism applies to <i>pcchDescriptionBuf</i>.
			

When making multiple calls to 
<b>MsiEnumComponentQualifiers</b> to enumerate all of the component's advertised qualifiers, each call should be made from the same thread.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

