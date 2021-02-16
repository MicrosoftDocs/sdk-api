---
UID: NF:mbnapi.IMbnPinManager.GetPin
title: IMbnPinManager::GetPin (mbnapi.h)
description: Gets a specific type of PIN.
helpviewer_keywords: ["GetPin","GetPin method [Microsoft Broadband Networks]","GetPin method [Microsoft Broadband Networks]","IMbnPinManager interface","IMbnPinManager interface [Microsoft Broadband Networks]","GetPin method","IMbnPinManager.GetPin","IMbnPinManager::GetPin","mbn.imbnpinmanager_getpin","mbnapi/IMbnPinManager::GetPin"]
old-location: mbn\imbnpinmanager_getpin.htm
tech.root: mbn
ms.assetid: 21752fb9-db6b-4fd1-9c6f-a756408bda53
ms.date: 12/05/2018
ms.keywords: GetPin, GetPin method [Microsoft Broadband Networks], GetPin method [Microsoft Broadband Networks],IMbnPinManager interface, IMbnPinManager interface [Microsoft Broadband Networks],GetPin method, IMbnPinManager.GetPin, IMbnPinManager::GetPin, mbn.imbnpinmanager_getpin, mbnapi/IMbnPinManager::GetPin
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
 - IMbnPinManager::GetPin
 - mbnapi/IMbnPinManager::GetPin
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
 - IMbnPinManager.GetPin
---

# IMbnPinManager::GetPin


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a specific type of PIN.

## -parameters

### -param pinType [in]

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_pin_type">MBN_PIN_TYPE</a> value that represents the requested PIN type.

### -param pin [out, retval]

Pointer to the address of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> for the requested PIN type.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  Otherwise, the calling application must release this interface when it is done using it.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The PIN type is not available.  The Mobile Broadband service is currently probing the device to retrieve this information.  When the PIN type is available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanagerevents-onpinlistavailable">OnPinListAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required for the operation to complete.  The calling Application can retry this operation when device is PIN unlocked

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
There is no SIM in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
There is a bad SIM in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The requested PIN type is not supported by the device.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>