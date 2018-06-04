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

# IUnknown_QueryService function


## -description


Retrieves an interface for a service from a specified object.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> instance of the COM object that supports the service.


### -param guidService [in]

Type: <b>REFGUID</b>

The service's unique identifier (SID).


### -param riid [in]

Type: <b>REFIID</b>

The IID of the desired service interface.


### -param ppvOut [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested <i>riid</i>. If successful, the calling application is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> using this value when the service is no longer needed. In the case of failure, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful. Returns <b>E_FAIL</b> if the object does not support <a href="_inet_IServiceProvider_Interface">IServiceProvider</a>. Otherwise, the function returns the <b>HRESULT</b> returned by the object's <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> method.




## -remarks



If the object passed in the <i>punk</i> parameter supports the <a href="_inet_IServiceProvider_Interface">IServiceProvider</a> interface, then its <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> method is invoked, passing the <i>guidService</i>, <i>riid</i>, and <i>ppvOut</i> parameters and propagating the return value. Otherwise, the function returns E_FAIL.

For those versions of Windows that do not include <b>IUnknown_QueryService</b> in Shlwapi.h, this function must be called directly from Shlwapi.dll using ordinal 176.




## -see-also




<a href="_inet_IServiceProvider_Interface">IServiceProvider</a>



<a href="_inet_IServiceProvider_QueryService_Method">QueryService</a>
 

 

