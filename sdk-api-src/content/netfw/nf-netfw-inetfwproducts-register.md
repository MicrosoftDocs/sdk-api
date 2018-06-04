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

# INetFwProducts::Register


## -description


The <b>Register</b> method registers a third-party firewall product.


## -parameters




### -param product [in]

The <a href="https://msdn.microsoft.com/e4cadbfd-d48d-4b38-a068-fc005d6f72af">INetFwProduct</a> object that defines the product to be registered.


### -param registration [out, retval]

The registration handle. The registration will be removed when this object is released.


## -returns




						If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_CANNOT_INSTALL</b></dt>
</dl>
</td>
<td width="60%">
The product binary has not been signed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid pointer.

</td>
</tr>
</table>
 




## -remarks



Registrations only last for the lifetime of the Windows Firewall service. Third-party firewalls calling this API should also have a service dependency on the Windows Firewall service (mpssvc) to make sure that  the service is not unexpectedly stopped, causing all registrations to be  lost.

Registrations are removed when a returned registration object is released by the third-party firewall or when the third-party firewall process exits.

A user mode code module using this API should be linked with the /integritycheck linker flag. This flag sets  <a href="https://msdn.microsoft.com/b6a50ffc-49f8-4824-9b51-7e381eaf8852">IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY</a> in the image PE header OptionalHeader.DllCharacteristics field, which  enforces a signature check at load time.  The code module should be digitally signed, consistent with the Authenticode signing procedure.




## -see-also




<a href="https://msdn.microsoft.com/e4cadbfd-d48d-4b38-a068-fc005d6f72af">INetFwProduct</a>



<a href="https://msdn.microsoft.com/66608887-02df-4caf-91d0-e5091849ff32">INetFwProducts</a>
 

 

