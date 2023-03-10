---
UID: NF:mfidl.IMFRemoteProxy.GetRemoteObject
title: IMFRemoteProxy::GetRemoteObject (mfidl.h)
description: Retrieves a pointer to the remote object for which this object is a proxy.
helpviewer_keywords: ["2d9e35bd-fe4c-4a98-91c8-2192ae34b2b3","GetRemoteObject","GetRemoteObject method [Media Foundation]","GetRemoteObject method [Media Foundation]","IMFRemoteProxy interface","IMFRemoteProxy interface [Media Foundation]","GetRemoteObject method","IMFRemoteProxy.GetRemoteObject","IMFRemoteProxy::GetRemoteObject","mf.imfremoteproxy_getremoteobject","mfidl/IMFRemoteProxy::GetRemoteObject"]
old-location: mf\imfremoteproxy_getremoteobject.htm
tech.root: mf
ms.assetid: 2d9e35bd-fe4c-4a98-91c8-2192ae34b2b3
ms.date: 12/05/2018
ms.keywords: 2d9e35bd-fe4c-4a98-91c8-2192ae34b2b3, GetRemoteObject, GetRemoteObject method [Media Foundation], GetRemoteObject method [Media Foundation],IMFRemoteProxy interface, IMFRemoteProxy interface [Media Foundation],GetRemoteObject method, IMFRemoteProxy.GetRemoteObject, IMFRemoteProxy::GetRemoteObject, mf.imfremoteproxy_getremoteobject, mfidl/IMFRemoteProxy::GetRemoteObject
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
 - IMFRemoteProxy::GetRemoteObject
 - mfidl/IMFRemoteProxy::GetRemoteObject
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
 - IMFRemoteProxy.GetRemoteObject
---

# IMFRemoteProxy::GetRemoteObject


## -description

Retrieves a pointer to the remote object for which this object is a proxy.

## -parameters

### -param riid [in]

Interface identifier (IID) of the requested interface.

### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy">IMFRemoteProxy</a>