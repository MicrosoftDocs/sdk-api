---
UID: NF:functiondiscoveryapi.IFunctionDiscovery.GetInstance
title: IFunctionDiscovery::GetInstance (functiondiscoveryapi.h)
author: windows-sdk-content
description: Gets the specified function instance, based on identifier.
old-location: ncd\ifunctiondiscovery_getinstance_method.htm
tech.root: FunDisc
ms.assetid: 8f3b2517-0acf-4a43-9539-d905c78be426
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInstance, GetInstance method, GetInstance method,IFunctionDiscovery interface, IFunctionDiscovery interface,GetInstance method, IFunctionDiscovery.GetInstance, IFunctionDiscovery::GetInstance, functiondiscoveryapi/IFunctionDiscovery::GetInstance, ncd.ifunctiondiscovery_getinstance_method
ms.topic: method
f1_keywords: 
 - "functiondiscoveryapi/IFunctionDiscovery.GetInstance"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionDiscovery::GetInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified function instance, based on identifier.


## -parameters




### -param pszFunctionInstanceIdentity [in]

The identifier of the function instance (see <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-getid">GetID</a>). 


### -param ppIFunctionInstance [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface pointer used to return the interface.


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



Some function discovery providers return their query results with the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface.  <b>GetInstance</b> does not find function instances that are returned in this way and will fail with E_PENDING.  It is recommended that clients use the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery">CreateInstanceQuery</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a> interface to find function instances for such providers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscovery">IFunctionDiscovery</a>
 

 

