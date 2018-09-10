---
UID: NF:wcndevice.IWCNDevice.SetVendorExtension
title: IWCNDevice::SetVendorExtension
author: windows-sdk-content
description: The IWCNDevice::SetVendorExtension method queues a vendor extension for use in the pending session. This function may only be called prior to IWCNDevice::Connect.
old-location: wcn\iwcndevice_setvendorextension.htm
tech.root: wcn
ms.assetid: ed96b9bc-4f4e-48bb-9c1d-8a0ababe0b26
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWCNDevice interface [Windows Connect Now],SetVendorExtension method, IWCNDevice.SetVendorExtension, IWCNDevice::SetVendorExtension, SetVendorExtension, SetVendorExtension method [Windows Connect Now], SetVendorExtension method [Windows Connect Now],IWCNDevice interface, wcn.iwcndevice_setvendorextension, wcndevice/IWCNDevice::SetVendorExtension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
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
 - WcnDevice.h
api_name:
 - IWCNDevice.SetVendorExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCNDevice::SetVendorExtension


## -description


The <b>IWCNDevice::SetVendorExtension</b> method queues a vendor extension for use in the pending session.  This function may only be called prior to <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a>.


## -parameters




### -param pVendorExtSpec [in]

A pointer to a <b>WCN_VENDOR_EXTENSION_SPEC</b> structure that contains the vendor extension specification.


### -param cbBuffer [in]

The number of bytes contained in <i>pbBuffer</i>.


### -param pbBuffer [in]

Pointer to a buffer that contains the data to set in the vendor extension.


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
The vendor extension will be sent in the pending session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <b>WCN_VENDOR_EXTENSION_SPEC</b> contains an illegal VendorID, sub-type, or flag. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_IMPLEMENTATION_LIMIT)</b></dt>
</dl>
</td>
<td width="60%">
The number of vendor extensions has exceeded the current implementation limit, which is currently equal to 25 vendor extensions per session.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a>



<a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a>



<b>WCN_VENDOR_EXTENSION_SPEC</b>
 

 

