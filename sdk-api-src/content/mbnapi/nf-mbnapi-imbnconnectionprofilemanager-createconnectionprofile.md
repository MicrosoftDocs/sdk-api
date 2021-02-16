---
UID: NF:mbnapi.IMbnConnectionProfileManager.CreateConnectionProfile
title: IMbnConnectionProfileManager::CreateConnectionProfile (mbnapi.h)
description: Creates a new connection profile for the device.
helpviewer_keywords: ["CreateConnectionProfile","CreateConnectionProfile method [Microsoft Broadband Networks]","CreateConnectionProfile method [Microsoft Broadband Networks]","IMbnConnectionProfileManager interface","IMbnConnectionProfileManager interface [Microsoft Broadband Networks]","CreateConnectionProfile method","IMbnConnectionProfileManager.CreateConnectionProfile","IMbnConnectionProfileManager::CreateConnectionProfile","mbn.imbnconnectionprofilemanager_createconnectionprofile","mbnapi/IMbnConnectionProfileManager::CreateConnectionProfile"]
old-location: mbn\imbnconnectionprofilemanager_createconnectionprofile.htm
tech.root: mbn
ms.assetid: b9c191cc-aa6f-4548-ad4a-f2b9808c5f23
ms.date: 12/05/2018
ms.keywords: CreateConnectionProfile, CreateConnectionProfile method [Microsoft Broadband Networks], CreateConnectionProfile method [Microsoft Broadband Networks],IMbnConnectionProfileManager interface, IMbnConnectionProfileManager interface [Microsoft Broadband Networks],CreateConnectionProfile method, IMbnConnectionProfileManager.CreateConnectionProfile, IMbnConnectionProfileManager::CreateConnectionProfile, mbn.imbnconnectionprofilemanager_createconnectionprofile, mbnapi/IMbnConnectionProfileManager::CreateConnectionProfile
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
 - IMbnConnectionProfileManager::CreateConnectionProfile
 - mbnapi/IMbnConnectionProfileManager::CreateConnectionProfile
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
 - IMbnConnectionProfileManager.CreateConnectionProfile
---

# IMbnConnectionProfileManager::CreateConnectionProfile


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Creates a new connection profile for the device.

## -parameters

### -param xmlProfile [in]

A null-terminated string that contains the profile data in XML format compliant with the <a href="/windows/desktop/mbn/schema-schema">Mobile Broadband Profile Schema Reference</a>.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
A profile with the given name already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_INVALID_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The profile does not conform to the Mobile Broadband profile schema.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The icon file location passed in the profile is not valid or not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_DEFAULT_PROFILE_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The calling application specified the default profile flag in the XML data, however the default profile already exists for the Mobile Broadband device.

</td>
</tr>
</table>

## -remarks

This is a synchronous operation. If this function call is successful, then a new profile will be created and the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanagerevents-onconnectionprofilearrival">OnConnectionProfileArrival</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a> interface. 


If the icon file location is specified in the profile data then the Mobile Broadband service will copy the icon file from the specified location in its own store. A subsequent query on the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> object for the icon file location will return the file location where the Mobile Broadband service stored the icon file. Whenever a profile is deleted from the system, its icon file is also deleted from the system. The icon file should be in bmp file format file with 32x32 pixel dimensions.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a>