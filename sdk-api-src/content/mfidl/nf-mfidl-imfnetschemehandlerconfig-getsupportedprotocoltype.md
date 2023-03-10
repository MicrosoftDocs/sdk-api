---
UID: NF:mfidl.IMFNetSchemeHandlerConfig.GetSupportedProtocolType
title: IMFNetSchemeHandlerConfig::GetSupportedProtocolType (mfidl.h)
description: Retrieves a supported protocol by index.
helpviewer_keywords: ["51cd90cf-a3ae-45dd-bc27-c91d44cab9f5","GetSupportedProtocolType","GetSupportedProtocolType method [Media Foundation]","GetSupportedProtocolType method [Media Foundation]","IMFNetSchemeHandlerConfig interface","IMFNetSchemeHandlerConfig interface [Media Foundation]","GetSupportedProtocolType method","IMFNetSchemeHandlerConfig.GetSupportedProtocolType","IMFNetSchemeHandlerConfig::GetSupportedProtocolType","mf.imfnetschemehandlerconfig_getsupportedprotocoltype","mfidl/IMFNetSchemeHandlerConfig::GetSupportedProtocolType"]
old-location: mf\imfnetschemehandlerconfig_getsupportedprotocoltype.htm
tech.root: mf
ms.assetid: 51cd90cf-a3ae-45dd-bc27-c91d44cab9f5
ms.date: 12/05/2018
ms.keywords: 51cd90cf-a3ae-45dd-bc27-c91d44cab9f5, GetSupportedProtocolType, GetSupportedProtocolType method [Media Foundation], GetSupportedProtocolType method [Media Foundation],IMFNetSchemeHandlerConfig interface, IMFNetSchemeHandlerConfig interface [Media Foundation],GetSupportedProtocolType method, IMFNetSchemeHandlerConfig.GetSupportedProtocolType, IMFNetSchemeHandlerConfig::GetSupportedProtocolType, mf.imfnetschemehandlerconfig_getsupportedprotocoltype, mfidl/IMFNetSchemeHandlerConfig::GetSupportedProtocolType
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetSchemeHandlerConfig::GetSupportedProtocolType
 - mfidl/IMFNetSchemeHandlerConfig::GetSupportedProtocolType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetSchemeHandlerConfig.GetSupportedProtocolType
---

# IMFNetSchemeHandlerConfig::GetSupportedProtocolType


## -description

Retrieves a supported protocol by index

## -parameters

### -param nProtocolIndex [in]

Zero-based index of the protocol to retrieve. To get the number of supported protocols, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols">IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols</a>.

### -param pnProtocolType [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type">MFNETSOURCE_PROTOCOL_TYPE</a> enumeration.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>nProtocolIndex</i> parameter was greater than the total number of supported protocols, returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols">GetNumberOfSupportedProtocols</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig">IMFNetSchemeHandlerConfig</a>