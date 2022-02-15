---
UID: NF:mbnapi.IMbnConnectionProfile.Delete
title: IMbnConnectionProfile::Delete (mbnapi.h)
description: Deletes the profile from the system.
helpviewer_keywords: ["Delete","Delete method [Microsoft Broadband Networks]","Delete method [Microsoft Broadband Networks]","IMbnConnectionProfile interface","IMbnConnectionProfile interface [Microsoft Broadband Networks]","Delete method","IMbnConnectionProfile.Delete","IMbnConnectionProfile::Delete","mbn.imbnconnectionprofile_delete","mbnapi/IMbnConnectionProfile::Delete"]
old-location: mbn\imbnconnectionprofile_delete.htm
tech.root: mbn
ms.assetid: 4de7da76-c873-4a57-a021-17436d1a64a4
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Microsoft Broadband Networks], Delete method [Microsoft Broadband Networks],IMbnConnectionProfile interface, IMbnConnectionProfile interface [Microsoft Broadband Networks],Delete method, IMbnConnectionProfile.Delete, IMbnConnectionProfile::Delete, mbn.imbnconnectionprofile_delete, mbnapi/IMbnConnectionProfile::Delete
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
 - IMbnConnectionProfile::Delete
 - mbnapi/IMbnConnectionProfile::Delete
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
 - IMbnConnectionProfile.Delete
---

# IMbnConnectionProfile::Delete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Deletes the profile from the system.



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
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
</table>

## -remarks

This is an asynchronous operation.  The Mobile Broadband service will notify the calling application by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanagerevents-onconnectionprofileremoval">OnConnectionProfileRemoval</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a>
