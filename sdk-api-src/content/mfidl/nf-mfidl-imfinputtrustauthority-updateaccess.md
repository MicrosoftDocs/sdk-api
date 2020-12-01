---
UID: NF:mfidl.IMFInputTrustAuthority.UpdateAccess
title: IMFInputTrustAuthority::UpdateAccess (mfidl.h)
description: Notifies the input trust authority (ITA) when the number of output trust authorities (OTAs) that will perform a specified action has changed.
helpviewer_keywords: ["4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176","IMFInputTrustAuthority interface [Media Foundation]","UpdateAccess method","IMFInputTrustAuthority.UpdateAccess","IMFInputTrustAuthority::UpdateAccess","UpdateAccess","UpdateAccess method [Media Foundation]","UpdateAccess method [Media Foundation]","IMFInputTrustAuthority interface","mf.imfinputtrustauthority_updateaccess","mfidl/IMFInputTrustAuthority::UpdateAccess"]
old-location: mf\imfinputtrustauthority_updateaccess.htm
tech.root: mf
ms.assetid: 4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176
ms.date: 12/05/2018
ms.keywords: 4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176, IMFInputTrustAuthority interface [Media Foundation],UpdateAccess method, IMFInputTrustAuthority.UpdateAccess, IMFInputTrustAuthority::UpdateAccess, UpdateAccess, UpdateAccess method [Media Foundation], UpdateAccess method [Media Foundation],IMFInputTrustAuthority interface, mf.imfinputtrustauthority_updateaccess, mfidl/IMFInputTrustAuthority::UpdateAccess
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFInputTrustAuthority::UpdateAccess
 - mfidl/IMFInputTrustAuthority::UpdateAccess
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
 - IMFInputTrustAuthority.UpdateAccess
---

# IMFInputTrustAuthority::UpdateAccess


## -description

Notifies the input trust authority (ITA) when the number of output trust authorities (OTAs) that will perform a specified action has changed.

## -parameters

### -param pParam [in]

Pointer to an <a href="/windows/desktop/api/mfidl/ns-mfidl-mfinputtrustauthority_access_params">MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS</a> structure that contains parameters for the <b>UpdateAccess</b> action.

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
</table>

## -remarks

The ITA can update its internal state if needed. If the method returns a failure code, the Media Session cancels the action.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>