---
UID: NF:wcndevice.IWCNDevice.GetVendorExtension
title: IWCNDevice::GetVendorExtension (wcndevice.h)
description: The GetVendorExtension method gets a cached vendor extension from the device.
helpviewer_keywords: ["GetVendorExtension","GetVendorExtension method [Windows Connect Now]","GetVendorExtension method [Windows Connect Now]","IWCNDevice interface","IWCNDevice interface [Windows Connect Now]","GetVendorExtension method","IWCNDevice.GetVendorExtension","IWCNDevice::GetVendorExtension","wcn.iwcndevice_getvendorextension","wcndevice/IWCNDevice::GetVendorExtension"]
old-location: wcn\iwcndevice_getvendorextension.htm
tech.root: wcn
ms.assetid: f7fa8446-8013-431a-95ed-fa5d78a90df7
ms.date: 12/05/2018
ms.keywords: GetVendorExtension, GetVendorExtension method [Windows Connect Now], GetVendorExtension method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetVendorExtension method, IWCNDevice.GetVendorExtension, IWCNDevice::GetVendorExtension, wcn.iwcndevice_getvendorextension, wcndevice/IWCNDevice::GetVendorExtension
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWCNDevice::GetVendorExtension
 - wcndevice/IWCNDevice::GetVendorExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.GetVendorExtension
---

# IWCNDevice::GetVendorExtension


## -description

The <b>GetVendorExtension</b> method gets a cached vendor extension from the device.

## -parameters

### -param pVendorExtSpec [in]

A pointer to a user-defined <b>WCN_VENDOR_EXTENSION_SPEC</b> structure that describes the vendor extension to query for.

### -param dwMaxBufferSize [in]

The size, in bytes, of <i>pbBuffer</i>.

### -param pbBuffer [out]

An allocated buffer that,  on return, contains the contents of the  vendor extension.

### -param pdwBufferUsed [out]

On return, contains the size of the vendor extension in bytes.

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
The vendor extension was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The vendor extension specified is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>pbBuffer</i> is not large enough to contain the returned vendor extension.

</td>
</tr>
</table>

## -remarks

 To query the size of a vendor extension, you can pass a value of 0 with the <i>dwMaxBufferSize</i> parameter, and <i>pdwBufferUsed</i> will receive the size.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>