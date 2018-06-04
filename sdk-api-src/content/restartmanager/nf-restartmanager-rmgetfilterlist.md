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

# RmGetFilterList function


## -description


Lists the modifications to shutdown and restart actions that have already been applied by the <a href="https://msdn.microsoft.com/63d1d1d2-d7b7-4d6c-99f9-b849229e171f">RmAddFilter</a> function. The function returns a pointer to a buffer containing information about the modifications which have been applied.


## -parameters




### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.


### -param pbFilterBuf [out, optional]

A pointer to a buffer that contains modification information.


### -param cbFilterBuf [in]

The size of the buffer that contains modification information in bytes.


### -param cbFilterBufNeeded [out]

The number of bytes needed in the buffer.


## -returns



This is the most recent error received. The function can return one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a> that are defined in Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in as a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234</dt>
</dl>
</td>
<td width="60%">
This error value is returned by the <a href="https://msdn.microsoft.com/61427838-8b23-4105-93fd-55f457fd43a7">RmGetFilterList</a> function if the <i>pbFilterBuf</i> buffer is too small to hold all the application information in the list or if <i>cbFilterBufNeeded</i> was not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SESSION_CREDENTIAL_CONFLICT</b></dt>
<dt> 1219</dt>
</dl>
</td>
<td width="60%">
This error is returned when a secondary installer calls this function. This function is only available to primary installers.

</td>
</tr>
</table>
 




## -remarks



The returned <i>pbFilterBuf</i> buffer has to be typecast to <b>RM_FILTER_INFO</b> to access the filter list.




## -see-also




<a href="https://msdn.microsoft.com/63d1d1d2-d7b7-4d6c-99f9-b849229e171f">RmAddFilter</a>
 

 

