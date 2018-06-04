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

# ICallFactory::CreateCall


## -description


Creates an instance of the call object that corresponds to a specified asynchronous interface.


## -parameters




### -param riid [in]

A reference to the identifier for the asynchronous interface.


### -param pCtrlUnk [in]

A pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the call object. If this parameter is not <b>NULL</b>, the call object is aggregated in the specified object.
If this parameter is <b>NULL</b>, the call object is not aggregated.


### -param riid2 [in]

The identifier of an interface on the call object. Typical values are IID_IUnknown and IID_ISynchronize.


### -param ppv [out]

The address of a pointer to the interface specified by <i>riid2</i>. This parameter cannot be <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The call object was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>riid</i> parameter does not reference the identifier for the asynchronous interface, such as IID_AsyncIEventSourceCallback.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/323dc627-3867-4170-b278-0bce46077729">ICallFactory</a>
 

 

