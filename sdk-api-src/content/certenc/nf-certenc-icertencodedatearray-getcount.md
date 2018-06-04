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

# ICertEncodeDateArray::GetCount


## -description


The <b>GetCount</b> method returns the number of <b>DATE</b> values in the object's <b>DATE</b> array.


## -parameters




### -param pCount [out]

A pointer to a <b>LONG</b> that receives the number of <b>DATE</b> values contained in the <b>DATE</b> array.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of <b>DATE</b> values contained in the <b>DATE</b> array.




## -see-also




<a href="https://msdn.microsoft.com/9973c49a-d886-4cc4-b75e-7ff46f56d51c">ICertEncodeDateArray</a>



<a href="https://msdn.microsoft.com/db108b2a-c3ee-4ef8-be5c-74dc739dacee">ICertEncodeDateArray::GetValue</a>



<a href="https://msdn.microsoft.com/f09087aa-ae10-4a59-9b59-5f8b72254ce6">ICertEncodeDateArray::Reset</a>
 

 

