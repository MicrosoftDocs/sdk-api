---
UID: NF:mbnapi.IMbnServiceActivation.Activate
title: IMbnServiceActivation::Activate
author: windows-sdk-content
description: Send the service activation request to the network.
old-location: mbn\imbnserviceactivation_activate.htm
tech.root: mbn
ms.assetid: 3c131363-9403-4c7a-984d-6602b879c08e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Activate, Activate method [Microsoft Broadband Networks], Activate method [Microsoft Broadband Networks],IMbnServiceActivation interface, IMbnServiceActivation interface [Microsoft Broadband Networks],Activate method, IMbnServiceActivation.Activate, IMbnServiceActivation::Activate, mbn.imbnserviceactivation_activate, mbnapi/IMbnServiceActivation::Activate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnServiceActivation.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mbnapi.h
: 
- IMbnServiceActivation.Activate
: 
---

# IMbnServiceActivation::Activate


## -description


Send the service activation request to the network.


## -parameters




### -param vendorSpecificData [in]

A vendor-specific array of bytes passed in a service activation operation. This data will be passed by the Mobile Broadband service in a SET OID_WWAN_SERVICE_ACTIVATION  OID request to the miniport driver.


### -param requestID [out]

The request ID for this operation.


## -returns



This method can return one of these values.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid. Most likely the Mobile Broadband device has been removed from the system.

Invalid interface.  Most likely the device has been removed from the system.

</td>
</tr>
</table>
 




## -remarks



The <b>Activate</b> method can be used by an application to activate cellular service. The format of data passed in this request is vendor-specific.

The <b>VendorSpecificBufferSize</b> field of the OID request would be set to the size of data in the SAFEARRAY,  <i>vendorSpecificData</i>. The contents of <i>vendorSpecificData</i> will be copied byte-by-byte in the OID request to the driver.

Refer to the Mobile Broadband Driver Model for more information about service activation operations.


This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/bc1c85b3-1b7b-4439-9358-801da8f4c79b">OnActivationComplete</a> method of the  <a href="https://msdn.microsoft.com/b3385523-f1ab-403d-9244-7683a7e9f95a">IMbnServiceActivationEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/cf23be24-f7a8-41b9-81f1-c267a265f85b">IMbnServiceActivation</a>
 

 

