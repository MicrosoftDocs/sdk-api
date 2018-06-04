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

# IGPM::GetClientSideExtensions


## -description


Creates and returns a 
<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">GPMCSECollection</a> object that allows you to enumerate Group Policy client-side extensions (CSEs) that are registered on the local computer.


## -parameters




### -param ppIGPMCSECollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">IGPMCSECollection</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMCSECollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMCSECollection</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">IGPMCSECollection</a>
 

 

