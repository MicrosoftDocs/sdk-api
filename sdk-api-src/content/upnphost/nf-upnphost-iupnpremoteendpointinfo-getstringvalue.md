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

# IUPnPRemoteEndpointInfo::GetStringValue


## -description


The <b>GetStringValue</b> method gets a string that provides information about either a request or requester.


## -parameters




### -param bstrValueName [in]

String that specifies the category of information to be retrieved.


### -param pbstrValue [out]

Pointer to a string, the meaning of which depends on the value of <i>bstrValueName</i>.

If <i>bstrValueName</i> is "RemoteAddress", the string is the requester's IP address.<b>Windows 7:  </b>To retrieve the HTTP UserAgent header, set <i>bstrValueName</i> to "HttpUserAgent".




## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Currently, the only valid values for the <i>bstrValueName</i> parameter are "RemoteAddress" and (Windows 7 only) "HttpUserAgent". For any other value, this method will return the COM error code E_INVALIDARG.






## -see-also




<a href="https://msdn.microsoft.com/efbb0671-cb32-41e1-8405-1d145c247673">GetDwordValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff597612">GetGuidValue</a>



<a href="https://msdn.microsoft.com/32e246cd-50eb-4221-8166-a7cd8ed42d69">IUPnPRemoteEndpointInfo</a>
 

 

