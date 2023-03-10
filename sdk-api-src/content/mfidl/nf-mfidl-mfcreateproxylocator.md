---
UID: NF:mfidl.MFCreateProxyLocator
title: MFCreateProxyLocator function (mfidl.h)
description: Creates a default proxy locator.
helpviewer_keywords: ["9ad707df-533a-407b-a611-49bfb019affc","MFCreateProxyLocator","MFCreateProxyLocator function [Media Foundation]","mf.mfcreateproxylocator","mfidl/MFCreateProxyLocator"]
old-location: mf\mfcreateproxylocator.htm
tech.root: mf
ms.assetid: 9ad707df-533a-407b-a611-49bfb019affc
ms.date: 12/05/2018
ms.keywords: 9ad707df-533a-407b-a611-49bfb019affc, MFCreateProxyLocator, MFCreateProxyLocator function [Media Foundation], mf.mfcreateproxylocator, mfidl/MFCreateProxyLocator
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateProxyLocator
 - mfidl/MFCreateProxyLocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateProxyLocator
---

# MFCreateProxyLocator function


## -description

Creates a default proxy locator.

## -parameters

### -param pszProtocol [in]

The name of the protocol.

<div class="alert"><b>Note</b>  In this release of Media Foundation, the default proxy locator does not support RTSP.</div>
<div> </div>

### -param pProxyConfig [in]

Pointer to the <b>IPropertyStore</b> interface of a property store that contains the proxy configuration in the <a href="/windows/desktop/medfound/mfnetsource-proxysettings-property">MFNETSOURCE_PROXYSETTINGS</a> property.

### -param ppProxyLocator [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator">IMFNetProxyLocator</a> interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/proxy-support-for-network-sources">Proxy Support for Network Sources</a>