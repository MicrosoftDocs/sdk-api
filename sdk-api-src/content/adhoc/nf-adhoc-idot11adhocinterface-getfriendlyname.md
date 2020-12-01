---
UID: NF:adhoc.IDot11AdHocInterface.GetFriendlyName
title: IDot11AdHocInterface::GetFriendlyName (adhoc.h)
description: Gets the friendly name of the NIC.
helpviewer_keywords: ["GetFriendlyName","GetFriendlyName method [NativeWIFI]","GetFriendlyName method [NativeWIFI]","IDot11AdHocInterface interface","IDot11AdHocInterface interface [NativeWIFI]","GetFriendlyName method","IDot11AdHocInterface.GetFriendlyName","IDot11AdHocInterface::GetFriendlyName","adhoc/IDot11AdHocInterface::GetFriendlyName","nwifi.idot11adhocinterface_getfriendlyname"]
old-location: nwifi\idot11adhocinterface_getfriendlyname.htm
tech.root: nwifi
ms.assetid: 945947e9-99ea-4420-95db-5b831e59e894
ms.date: 12/05/2018
ms.keywords: GetFriendlyName, GetFriendlyName method [NativeWIFI], GetFriendlyName method [NativeWIFI],IDot11AdHocInterface interface, IDot11AdHocInterface interface [NativeWIFI],GetFriendlyName method, IDot11AdHocInterface.GetFriendlyName, IDot11AdHocInterface::GetFriendlyName, adhoc/IDot11AdHocInterface::GetFriendlyName, nwifi.idot11adhocinterface_getfriendlyname
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - IDot11AdHocInterface::GetFriendlyName
 - adhoc/IDot11AdHocInterface::GetFriendlyName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocInterface.GetFriendlyName
---

# IDot11AdHocInterface::GetFriendlyName


## -description

Gets the friendly name of the NIC.

## -parameters

### -param ppszName [out]

The friendly name of the NIC. The SSID of the network is used as the friendly name.

You must free this string using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a>