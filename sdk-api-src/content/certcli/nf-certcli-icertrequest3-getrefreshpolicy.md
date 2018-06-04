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

# ICertRequest3::GetRefreshPolicy


## -description


The <b>GetRefreshPolicy</b> method returns a value that indicates whether a client's cached certificate enrollment policy is out of date and needs to be refreshed.


## -parameters




### -param pValue [out, retval]

A pointer to a <b>VARIANT_BOOL</b> variable to receive the refresh indicator.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>BOOL</b> that indicates whether the client's policy service is out of date.




## -remarks



The <b>GetRefreshPolicy</b> method returns <b>TRUE</b> only when the enrollment server returns a fault. Before calling the <b>GetRefreshPolicy</b> method you must contact the enrollment server. If a fault is returned, then call  the <b>GetRefreshPolicy</b> method from same instance of <a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a> to determine whether  the cached policy is out of date and needs to be refreshed.



