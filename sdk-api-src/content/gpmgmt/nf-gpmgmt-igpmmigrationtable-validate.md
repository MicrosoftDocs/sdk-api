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

# IGPMMigrationTable::Validate


## -description


Validates the migration table.


## -parameters




### -param ppResult [out]

Reference to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Result</b> property references whether the validation is successful. The <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property references the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> that contains the validation errors or warnings.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object. The <b>Result</b> property references whether the validation was successful. The <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property references the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">GPMStatusMsgCollection</a> that contains the validation errors or warnings.

<h3>VB</h3>
Returns a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object. The <b>Result</b> property references whether the validation was successful. The <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property references the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">GPMStatusMsgCollection</a> that contains the validation errors or warnings.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMMigrationTable</a>
 

 

