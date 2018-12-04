---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.GetInstance
title: IFunctionDiscovery::GetInstance
author: windows-sdk-content
description: Gets the specified function instance, based on identifier.
old-location: ncd\ifunctiondiscovery_getinstance_method.htm
tech.root: fundisc
ms.assetid: 8f3b2517-0acf-4a43-9539-d905c78be426
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetInstance, GetInstance method, GetInstance method,IFunctionDiscovery interface, IFunctionDiscovery interface,GetInstance method, IFunctionDiscovery.GetInstance, IFunctionDiscovery::GetInstance, functiondiscoveryapi/IFunctionDiscovery::GetInstance, ncd.ifunctiondiscovery_getinstance_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionDiscovery.GetInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscovery::GetInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified function instance, based on identifier.


## -parameters




### -param pszFunctionInstanceIdentity [in]

The identifier of the function instance (see <a href="https://msdn.microsoft.com/8a198bc4-cdec-4d46-a1a2-3952d4dc2a7d">GetID</a>). 


### -param ppIFunctionInstance [out]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface pointer used to return the interface.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code/value</th>
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
The value of <i>pszFunctionInstanceIdentity</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)</b></dt>
<dt>0x800710d8</dt>
</dl>
</td>
<td width="60%">
The function instance represented by the specified ID does not exist on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call was executed for a provider that returns results asynchronously.

</td>
</tr>
</table>
 




## -remarks



Some function discovery providers return their query results with the <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface.  <b>GetInstance</b> does not find function instances that are returned in this way and will fail with E_PENDING.  It is recommended that clients use the <a href="https://msdn.microsoft.com/80e70972-ced1-416e-aa4f-69c54b2cbf95">CreateInstanceQuery</a> method of the <a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a> interface to find function instances for such providers.




## -see-also




<a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>
 

 

