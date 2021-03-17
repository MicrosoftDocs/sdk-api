---
UID: NF:mfidl.IMFInputTrustAuthority.BindAccess
title: IMFInputTrustAuthority::BindAccess (mfidl.h)
description: Notifies the input trust authority (ITA) that a requested action is about to be performed.
helpviewer_keywords: ["94e447af-9311-4a2c-9ec5-be371684f79d","BindAccess","BindAccess method [Media Foundation]","BindAccess method [Media Foundation]","IMFInputTrustAuthority interface","IMFInputTrustAuthority interface [Media Foundation]","BindAccess method","IMFInputTrustAuthority.BindAccess","IMFInputTrustAuthority::BindAccess","mf.imfinputtrustauthority_bindaccess","mfidl/IMFInputTrustAuthority::BindAccess"]
old-location: mf\imfinputtrustauthority_bindaccess.htm
tech.root: mf
ms.assetid: 94e447af-9311-4a2c-9ec5-be371684f79d
ms.date: 12/05/2018
ms.keywords: 94e447af-9311-4a2c-9ec5-be371684f79d, BindAccess, BindAccess method [Media Foundation], BindAccess method [Media Foundation],IMFInputTrustAuthority interface, IMFInputTrustAuthority interface [Media Foundation],BindAccess method, IMFInputTrustAuthority.BindAccess, IMFInputTrustAuthority::BindAccess, mf.imfinputtrustauthority_bindaccess, mfidl/IMFInputTrustAuthority::BindAccess
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
 - IMFInputTrustAuthority::BindAccess
 - mfidl/IMFInputTrustAuthority::BindAccess
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
 - IMFInputTrustAuthority.BindAccess
---

# IMFInputTrustAuthority::BindAccess


## -description

Notifies the input trust authority (ITA) that a requested action is about to be performed.

## -parameters

### -param pParam [in]

Pointer to an <a href="/windows/desktop/api/mfidl/ns-mfidl-mfinputtrustauthority_access_params">MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS</a> structure that contains parameters for the <b>BindAccess</b> action.

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

Before calling this method, the Media Session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-requestaccess">IMFInputTrustAuthority::RequestAccess</a> to request an action. The <b>BindAccess</b> method notifies the ITA that the action is definitely about to occur, so that the ITA can update its internal state as needed. If the method returns a failure code, the Media Session cancels the action.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>