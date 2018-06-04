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

# IUpdateServiceManager::SetOption


## -description


Set options for the object that specifies the service ID. The <b>SetOption</b> method is also used to determine whether a warning is displayed when you change the registration of Automatic Updates.


## -parameters




### -param optionName [in]

Set this parameter to AllowedServiceID to specify the form of the service ID that is provided to the object. 

Set to AllowWarningUI to display a warning when changing the Automatic Updates registration.


### -param optionValue [in]

If the <i>optionName</i> parameter is set to AllowServiceID,    the <i>optionValue</i> parameter is set to the service ID that is provided as a <b>VT_BSTR</b> value.  

If <i>optionName</i> is set to AllowWarningUI,    <i>optionValue</i> is a <b>VT_BOOL</b> value that specifies whether to display a warning when changing the registration of Automatic Updates.

Set the optionValue parameter to VARIANT_TRUE to display the warning UI. Set it to VARIANT_FALSE to suppress the warning UI.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer is not allowed to access the update site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument of the method is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
 

 

