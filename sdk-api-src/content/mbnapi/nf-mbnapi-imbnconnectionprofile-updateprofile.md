---
UID: NF:mbnapi.IMbnConnectionProfile.UpdateProfile
title: IMbnConnectionProfile::UpdateProfile (mbnapi.h)
description: Updates the contents of the profile.
helpviewer_keywords: ["IMbnConnectionProfile interface [Microsoft Broadband Networks]","UpdateProfile method","IMbnConnectionProfile.UpdateProfile","IMbnConnectionProfile::UpdateProfile","UpdateProfile","UpdateProfile method [Microsoft Broadband Networks]","UpdateProfile method [Microsoft Broadband Networks]","IMbnConnectionProfile interface","mbn.imbnconnectionprofile_updateprofile","mbnapi/IMbnConnectionProfile::UpdateProfile"]
old-location: mbn\imbnconnectionprofile_updateprofile.htm
tech.root: mbn
ms.assetid: 3243ffec-1897-4f26-853d-81a7198a892d
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfile interface [Microsoft Broadband Networks],UpdateProfile method, IMbnConnectionProfile.UpdateProfile, IMbnConnectionProfile::UpdateProfile, UpdateProfile, UpdateProfile method [Microsoft Broadband Networks], UpdateProfile method [Microsoft Broadband Networks],IMbnConnectionProfile interface, mbn.imbnconnectionprofile_updateprofile, mbnapi/IMbnConnectionProfile::UpdateProfile
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
 - IMbnConnectionProfile::UpdateProfile
 - mbnapi/IMbnConnectionProfile::UpdateProfile
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
 - IMbnConnectionProfile.UpdateProfile
---

# IMbnConnectionProfile::UpdateProfile


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Updates the contents of the profile.

## -parameters

### -param strProfile [in]

A string that contains the profile data in XML format compliant with the <a href="/windows/desktop/mbn/schema-schema">Mobile Broadband Profile Schema Reference</a>.

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
The profile is invalid and likely has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR _NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The profile is invalid and has likely been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The profile data specifies an icon file that cannot be found at the indicated location.

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

The data provided by this method complies with the <a href="/windows/desktop/mbn/schema-schema">Mobile Broadband Profile Schema Reference</a>.

This method should be called when the device for the profile is present in the system.

This is a synchronous operation.  If successful, the Mobile Broadband service will notify the calling application by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofileevents-onprofileupdate">OnProfileUpdate</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofileevents">IMbnConnectionProfileEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a>