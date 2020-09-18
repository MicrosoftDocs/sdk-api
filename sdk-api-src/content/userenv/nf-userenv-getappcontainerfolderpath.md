---
UID: NF:userenv.GetAppContainerFolderPath
title: GetAppContainerFolderPath function (userenv.h)
description: Gets the path of the local app data folder for the specified app container.
helpviewer_keywords: ["GetAppContainerFolderPath","GetAppContainerFolderPath function [Windows Shell]","shell.getappcontainerfolderpath","userenv/GetAppContainerFolderPath"]
old-location: shell\getappcontainerfolderpath.htm
tech.root: shell
ms.assetid: 7D3AB78D-C094-4F89-8032-13F3C137E910
ms.date: 12/05/2018
ms.keywords: GetAppContainerFolderPath, GetAppContainerFolderPath function [Windows Shell], shell.getappcontainerfolderpath, userenv/GetAppContainerFolderPath
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
 - GetAppContainerFolderPath
 - userenv/GetAppContainerFolderPath
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
 - GetAppContainerFolderPath
---

# GetAppContainerFolderPath function


## -description

Gets the path of the local app data folder for the specified app container.

## -parameters

### -param pszAppContainerSid [in]

A pointer to the SID of the app container.

### -param ppszPath [out]

The address of a pointer to a string that, when this function returns successfully, receives the path of the local folder. It is the responsibility of the caller to free this string when it is no longer needed by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

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
The <i>pszAppContainerSid</i> or <i>ppszPath</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The path retrieved through this function is the same path that you would get by calling the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> function with <b>FOLDERID_LocalAppData</b>.

If a thread token is set, this function uses the app container for the current user. If no thread token is set, this function uses the app container associated with the process identity.

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-getappcontainerregistrylocation">GetAppContainerRegistryLocation</a>