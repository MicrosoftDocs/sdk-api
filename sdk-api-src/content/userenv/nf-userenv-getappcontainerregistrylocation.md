---
UID: NF:userenv.GetAppContainerRegistryLocation
title: GetAppContainerRegistryLocation function (userenv.h)
description: Gets the location of the registry storage associated with an app container.
helpviewer_keywords: ["GetAppContainerRegistryLocation","GetAppContainerRegistryLocation function [Windows Shell]","shell.getappcontainerregistrylocation","userenv/GetAppContainerRegistryLocation"]
old-location: shell\getappcontainerregistrylocation.htm
tech.root: shell
ms.assetid: DAD7EC07-D57D-40F5-AA99-AD7579910294
ms.date: 12/05/2018
ms.keywords: GetAppContainerRegistryLocation, GetAppContainerRegistryLocation function [Windows Shell], shell.getappcontainerregistrylocation, userenv/GetAppContainerRegistryLocation
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAppContainerRegistryLocation
 - userenv/GetAppContainerRegistryLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - GetAppContainerRegistryLocation
---

# GetAppContainerRegistryLocation function


## -description

Gets the location of the registry storage associated with an app container.

## -parameters

### -param desiredAccess [in]

Type: <b><a href="/windows/desktop/shell/messages">REGSAM</a></b>

The desired registry access.

### -param phAppContainerKey [out]

Type: <b>PHKEY</b>

A pointer to an HKEY that, when this function returns successfully, receives the registry storage location for the current profile.

## -returns

Type: <b>HRESULT</b>

This function returns an <b>HRESULT</b> code, including but not limited to the following:

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The caller is not running as or impersonating a user who can access this profile.

</td>
</tr>
</table>

## -remarks

The function gets the registry storage for the current user. To get the registry storage for another user, you must impersonate that user.

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-getappcontainerfolderpath">GetAppContainerFolderPath</a>