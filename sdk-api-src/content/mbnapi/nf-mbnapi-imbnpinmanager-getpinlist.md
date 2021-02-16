---
UID: NF:mbnapi.IMbnPinManager.GetPinList
title: IMbnPinManager::GetPinList (mbnapi.h)
description: Gets a list of different PIN types supported by the device.
helpviewer_keywords: ["GetPinList","GetPinList method [Microsoft Broadband Networks]","GetPinList method [Microsoft Broadband Networks]","IMbnPinManager interface","IMbnPinManager interface [Microsoft Broadband Networks]","GetPinList method","IMbnPinManager.GetPinList","IMbnPinManager::GetPinList","mbn.imbnpinmanager_getpinlist","mbnapi/IMbnPinManager::GetPinList"]
old-location: mbn\imbnpinmanager_getpinlist.htm
tech.root: mbn
ms.assetid: 732906dd-7d1e-49a1-a3cc-60075eed9c7c
ms.date: 12/05/2018
ms.keywords: GetPinList, GetPinList method [Microsoft Broadband Networks], GetPinList method [Microsoft Broadband Networks],IMbnPinManager interface, IMbnPinManager interface [Microsoft Broadband Networks],GetPinList method, IMbnPinManager.GetPinList, IMbnPinManager::GetPinList, mbn.imbnpinmanager_getpinlist, mbnapi/IMbnPinManager::GetPinList
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
 - IMbnPinManager::GetPinList
 - mbnapi/IMbnPinManager::GetPinList
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
 - IMbnPinManager.GetPinList
---

# IMbnPinManager::GetPinList


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a list of different PIN types supported by the device.

## -parameters

### -param pinList [out, retval]

A pointer to a list of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_pin_type">MBN_PIN_TYPE</a> values that represent the PIN types supported by the device.  When <b>GetPinList</b> returns anything other than <b>S_OK</b>, <i>pinList</i> is <b>NULL</b>, otherwise the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The PIN types are not available.  The Mobile Broadband service is currently probing the device to get the information.  When the PIN types are available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanagerevents-onpinlistavailable">OnPinListAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The device requires that a PIN must be entered for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
The SIM is not inserted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
</table>

## -remarks

On the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will attempt to retrieve this information from the device when the error condition is over. While it is retrieving this information <b>GetPinList</b> call will return <b>E_PENDING</b>. Once the retrieval operation is complete, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanagerevents-onpinlistavailable">OnPinListAvailable</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>