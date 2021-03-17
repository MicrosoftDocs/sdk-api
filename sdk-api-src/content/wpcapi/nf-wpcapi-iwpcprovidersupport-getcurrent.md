---
UID: NF:wpcapi.IWPCProviderSupport.GetCurrent
title: IWPCProviderSupport::GetCurrent (wpcapi.h)
description: Retrieves the GUID of the current provider.
helpviewer_keywords: ["GetCurrent","GetCurrent method","GetCurrent method","IWPCProviderSupport interface","IWPCProviderSupport interface","GetCurrent method","IWPCProviderSupport.GetCurrent","IWPCProviderSupport::GetCurrent","parcon.iwpcprovidersupport_getcurrent","wpcapi/IWPCProviderSupport::GetCurrent"]
old-location: parcon\iwpcprovidersupport_getcurrent.htm
tech.root: parcon
ms.assetid: 36496cba-229c-45bb-9608-04fb4b1955ae
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method, GetCurrent method,IWPCProviderSupport interface, IWPCProviderSupport interface,GetCurrent method, IWPCProviderSupport.GetCurrent, IWPCProviderSupport::GetCurrent, parcon.iwpcprovidersupport_getcurrent, wpcapi/IWPCProviderSupport::GetCurrent
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IWPCProviderSupport::GetCurrent
 - wpcapi/IWPCProviderSupport::GetCurrent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderSupport.GetCurrent
---

# IWPCProviderSupport::GetCurrent


## -description

Retrieves the GUID of the current provider.

## -parameters

### -param pguidProvider [out]

The GUID of the current provider.

## -returns

If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pguidProvider</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

The <i>pguidProvider</i> parameter will be a null GUID if there is no currently selected provider.

## -see-also

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcprovidersupport">IWPCProviderSupport</a>