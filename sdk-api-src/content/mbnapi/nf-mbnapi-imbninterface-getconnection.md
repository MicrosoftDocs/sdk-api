---
UID: NF:mbnapi.IMbnInterface.GetConnection
title: IMbnInterface::GetConnection (mbnapi.h)
description: Gets the IMbnConnection object.
helpviewer_keywords: ["GetConnection","GetConnection method [Microsoft Broadband Networks]","GetConnection method [Microsoft Broadband Networks]","IMbnInterface interface","IMbnInterface interface [Microsoft Broadband Networks]","GetConnection method","IMbnInterface.GetConnection","IMbnInterface::GetConnection","mbn.imbninterface_getconnection","mbnapi/IMbnInterface::GetConnection"]
old-location: mbn\imbninterface_getconnection.htm
tech.root: mbn
ms.assetid: 919772f5-1e86-424c-b3de-079a03bbc8e5
ms.date: 12/05/2018
ms.keywords: GetConnection, GetConnection method [Microsoft Broadband Networks], GetConnection method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetConnection method, IMbnInterface.GetConnection, IMbnInterface::GetConnection, mbn.imbninterface_getconnection, mbnapi/IMbnInterface::GetConnection
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnInterface::GetConnection
 - mbnapi/IMbnInterface::GetConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnInterface.GetConnection
---

# IMbnInterface::GetConnection


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> object associated with this interface.

## -parameters

### -param mbnConnection [out]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> object.

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
The method completed successfully.  <i>mbnConnection</i> contains a valid object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Either there is no available connection or the device is not registered to a network.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>