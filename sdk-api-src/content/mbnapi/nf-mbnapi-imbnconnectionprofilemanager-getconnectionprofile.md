---
UID: NF:mbnapi.IMbnConnectionProfileManager.GetConnectionProfile
title: IMbnConnectionProfileManager::GetConnectionProfile (mbnapi.h)
description: Gets a specific connection profile associated with the given Mobile Broadband device.
helpviewer_keywords: ["GetConnectionProfile","GetConnectionProfile method [Microsoft Broadband Networks]","GetConnectionProfile method [Microsoft Broadband Networks]","IMbnConnectionProfileManager interface","IMbnConnectionProfileManager interface [Microsoft Broadband Networks]","GetConnectionProfile method","IMbnConnectionProfileManager.GetConnectionProfile","IMbnConnectionProfileManager::GetConnectionProfile","mbn.imbnconnectionprofilemanager_getconnectionprofile","mbnapi/IMbnConnectionProfileManager::GetConnectionProfile"]
old-location: mbn\imbnconnectionprofilemanager_getconnectionprofile.htm
tech.root: mbn
ms.assetid: 24658f8b-a34f-4821-9fac-bd5c8810725f
ms.date: 12/05/2018
ms.keywords: GetConnectionProfile, GetConnectionProfile method [Microsoft Broadband Networks], GetConnectionProfile method [Microsoft Broadband Networks],IMbnConnectionProfileManager interface, IMbnConnectionProfileManager interface [Microsoft Broadband Networks],GetConnectionProfile method, IMbnConnectionProfileManager.GetConnectionProfile, IMbnConnectionProfileManager::GetConnectionProfile, mbn.imbnconnectionprofilemanager_getconnectionprofile, mbnapi/IMbnConnectionProfileManager::GetConnectionProfile
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnConnectionProfileManager::GetConnectionProfile
 - mbnapi/IMbnConnectionProfileManager::GetConnectionProfile
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
 - IMbnConnectionProfileManager.GetConnectionProfile
---

# IMbnConnectionProfileManager::GetConnectionProfile


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a specific connection profile associated with the given Mobile Broadband device.

## -parameters

### -param mbnInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device for which the profile request applies.  If <i>mbnInterface</i> is <b>NULL</b>, then this function will return the profile of the given name associated with any device in the system.

### -param profileName [in]

A null-terminated string that contains the name of the connection profile.

### -param connectionProfile [out, retval]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interface that represents the desired connection profile.  If this method returns anything other than <b>S_OK</b>, this is <b>NULL</b>.

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid, most likely because the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A profile with the given name does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_READY)</b></dt>
</dl>
</td>
<td width="60%">
The device is not ready.  Unable to obtain the subscriber ID because the device is  not <b>MBN_READY_STATE_INITIALIZED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A profile with the given name does not exist.

</td>
</tr>
</table>

## -remarks

A connection profile is associated with the subscriber ID of the device. For GSM devices the subscriber ID is the International Mobile Subscriber Identity (IMSI) of the SIM.  For CDMA devices it is the Mobile Identification Number (MIN) string or the International Roaming MIN (IRM) string. 

If a new profile has been created using <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile">CreateConnectionProfile</a>, then the caller must wait for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanagerevents-onconnectionprofilearrival">OnConnectionProfileArrival</a> event to be received before calling <b>GetConnectionProfile</b> with the new profile's name; otherwise, the <b>GetConnectionProfile</b> API call may fail with <b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a>