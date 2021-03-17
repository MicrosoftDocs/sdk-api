---
UID: NF:shimgdata.IShellImageData.GetProperties
title: IShellImageData::GetProperties (shimgdata.h)
description: Gets an IPropertySetStorage through which the properties of the image can be accessed.
helpviewer_keywords: ["GetProperties","GetProperties method [Windows Shell]","GetProperties method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetProperties method","IShellImageData.GetProperties","IShellImageData::GetProperties","_shell_IShellImageData_GetProperties","shell.IShellImageData_GetProperties","shimgdata/IShellImageData::GetProperties"]
old-location: shell\IShellImageData_GetProperties.htm
tech.root: shell
ms.assetid: 0fb59627-a31f-4c23-955f-3032c5814a5a
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [Windows Shell], GetProperties method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetProperties method, IShellImageData.GetProperties, IShellImageData::GetProperties, _shell_IShellImageData_GetProperties, shell.IShellImageData_GetProperties, shimgdata/IShellImageData::GetProperties
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
 - IShellImageData::GetProperties
 - shimgdata/IShellImageData::GetProperties
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
 - IShellImageData.GetProperties
---

# IShellImageData::GetProperties


## -description

Gets an <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> through which the properties of the image can be accessed.

## -parameters

### -param dwMode [in]

Type: <b>DWORD</b>

Not used, set to 0.

### -param ppPropSet [out]

Type: <b><a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>**</b>

The address of a pointer to the <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful or an error value otherwise, including the following:

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
The image has not been decoded or the decoding process failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppPropSet</i> pointer is not valid.
          

</td>
</tr>
</table>