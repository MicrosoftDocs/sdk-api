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

# ICertConfig::Next


## -description


The <b>Next</b> method retrieves the index of the next available Certificate Services server configuration in the configuration point. This method was first defined in the <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a> interface.


## -parameters




### -param pIndex [out]

A pointer to a <b>Long</b> variable that will contain the index of the enumerated configuration, or –1 if there are no more configurations to enumerate.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pIndex</i> parameter contains the index of the enumerated configuration.  If there are no more configurations to enumerate, the return value is S_FALSE, and the <i>pIndex</i> parameter points to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a value that specifies the index of the next available Certificate Services server configuration in the configuration point. If no more configurations are available, the method returns a value of –1.




## -see-also




<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/6bac5961-f9cc-4859-affa-aa7ed152ebfa">ICertConfig2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
 

 

