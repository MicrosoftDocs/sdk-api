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

# ICertConfig::Reset


## -description


The <b>Reset</b> method resets the configuration query <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> to point at the Certificate Services server configuration indexed on the specified configuration point. This method was first defined in the <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a> interface.

Each individual configuration indicates a specific Certificate Services server. Some Certificate Services servers may have multiple valid configurations in the configuration database.


## -parameters




### -param Index [in]

Specifies the configuration point used by the configuration query to index a Certificate Services server configuration. The first configuration is index zero.


### -param pCount [out]

A pointer to the number of configurations in the enterprise.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pCount</i> parameter points to a <b>Long</b> that contains the number of configurations in the enterprise.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of configurations in the enterprise.




## -see-also




<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/6bac5961-f9cc-4859-affa-aa7ed152ebfa">ICertConfig2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
 

 

