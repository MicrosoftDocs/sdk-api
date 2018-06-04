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

# IFunctionDiscoveryServiceProvider::Initialize


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Initializes an object that provides a specific interface that has been bound to the resource represented by the function instance.


## -parameters




### -param pIFunctionInstance




### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the object.


### -param ppv [out]

The interface pointer requested in <i>riid</i>. Upon successful return, <i>*ppv</i> contains the requested interface pointer. Upon failure, <i>*ppv</i> contains <b>NULL</b>.


#### - pFunctionInstance [in]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface that represents the underlying resource.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains an invalid argument.

</td>
</tr>
</table>
 




## -remarks



Any error code indicates failure. The provider should return an appropriate error code if it is unable to create the desired object.




## -see-also




<a href="https://msdn.microsoft.com/dbdf27dc-5fb9-49ef-9a9b-ffcd7b148479">IFunctionDiscoveryServiceProvider</a>
 

 

