---
UID: NF:shimgdata.IShellImageData.DisplayName
title: IShellImageData::DisplayName (shimgdata.h)
description: Gets the name of the file if IShellImageData was initialized on a file path. Otherwise, gets the name of the data stream.
helpviewer_keywords: ["DisplayName","DisplayName method [Windows Shell]","DisplayName method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","DisplayName method","IShellImageData.DisplayName","IShellImageData::DisplayName","_shell_IShellImageData_DisplayName","shell.IShellImageData_DisplayName","shimgdata/IShellImageData::DisplayName"]
old-location: shell\IShellImageData_DisplayName.htm
tech.root: shell
ms.assetid: d2e95a44-2bf7-43e1-9a29-950acc34d2a4
ms.date: 12/05/2018
ms.keywords: DisplayName, DisplayName method [Windows Shell], DisplayName method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],DisplayName method, IShellImageData.DisplayName, IShellImageData::DisplayName, _shell_IShellImageData_DisplayName, shell.IShellImageData_DisplayName, shimgdata/IShellImageData::DisplayName
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData::DisplayName
 - shimgdata/IShellImageData::DisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.DisplayName
---

# IShellImageData::DisplayName


## -description

Gets the name of the file if <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> was initialized on a file path. Otherwise, gets the name of the data stream.

## -parameters

### -param wszName [in, out]

Type: <b>LPWSTR</b>

A pointer to a buffer containing the display name as a Unicode string. On exit, the contents of the buffer are only valid when the method returns S_OK.

### -param cch [in]

Type: <b>UINT</b>

The size, in characters, of the buffer pointed to by <i>wszName</i>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The file name or stream name cannot be retrieved.

</td>
</tr>
</table>