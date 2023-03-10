---
UID: NF:mbnapi.IMbnConnectionProfileManager.GetConnectionProfiles
title: IMbnConnectionProfileManager::GetConnectionProfiles (mbnapi.h)
description: Gets a list of connection profiles associated with the device.
helpviewer_keywords: ["GetConnectionProfiles","GetConnectionProfiles method [Microsoft Broadband Networks]","GetConnectionProfiles method [Microsoft Broadband Networks]","IMbnConnectionProfileManager interface","IMbnConnectionProfileManager interface [Microsoft Broadband Networks]","GetConnectionProfiles method","IMbnConnectionProfileManager.GetConnectionProfiles","IMbnConnectionProfileManager::GetConnectionProfiles","mbn.imbnconnectionprofilemanager_getconnectionprofiles","mbnapi/IMbnConnectionProfileManager::GetConnectionProfiles"]
old-location: mbn\imbnconnectionprofilemanager_getconnectionprofiles.htm
tech.root: mbn
ms.assetid: 96752181-1135-4dcf-9c07-056dfbf2ca5f
ms.date: 12/05/2018
ms.keywords: GetConnectionProfiles, GetConnectionProfiles method [Microsoft Broadband Networks], GetConnectionProfiles method [Microsoft Broadband Networks],IMbnConnectionProfileManager interface, IMbnConnectionProfileManager interface [Microsoft Broadband Networks],GetConnectionProfiles method, IMbnConnectionProfileManager.GetConnectionProfiles, IMbnConnectionProfileManager::GetConnectionProfiles, mbn.imbnconnectionprofilemanager_getconnectionprofiles, mbnapi/IMbnConnectionProfileManager::GetConnectionProfiles
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
 - IMbnConnectionProfileManager::GetConnectionProfiles
 - mbnapi/IMbnConnectionProfileManager::GetConnectionProfiles
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
 - IMbnConnectionProfileManager.GetConnectionProfiles
---

# IMbnConnectionProfileManager::GetConnectionProfiles


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a list of connection profiles associated with the device.

## -parameters

### -param mbnInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device for which the profile request applies.  If this is <b>NULL</b>, the function will return all of the profiles that are present in the system.

### -param connectionProfiles [out, retval]

An array of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interfaces that represent all the available connection profiles for the device.  If this method returns anything other than <b>S_OK</b>, the array pointer is <b>NULL</b>, otherwise the calling application must eventually free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
</table>

## -remarks

 When this operation is called for a particular device, it returns a list of profiles which have the same subscriber ID as currently reported by device. The <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getsubscriberinformation">GetSubscriberInformation</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> can be used to obtain the subscriber ID associated with the interface.

A connection profile is associated with the subscriber ID of the device. For GSM devices the subscriber ID is the International Mobile Subscriber Identity (IMSI) of the SIM.  For CDMA devices it is the Mobile Identification Number (MIN) string or the International Roaming MIN (IRM) string.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a>