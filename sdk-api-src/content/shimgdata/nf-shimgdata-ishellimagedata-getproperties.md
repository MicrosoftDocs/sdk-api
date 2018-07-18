---
UID: NF:shimgdata.IShellImageData.GetProperties
title: IShellImageData::GetProperties
author: windows-sdk-content
description: Gets an IPropertySetStorage through which the properties of the image can be accessed.
old-location: shell\IShellImageData_GetProperties.htm
old-project: shell
ms.assetid: 0fb59627-a31f-4c23-955f-3032c5814a5a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetProperties, GetProperties method [Windows Shell], GetProperties method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetProperties method, IShellImageData.GetProperties, IShellImageData::GetProperties, _shell_IShellImageData_GetProperties, shell.IShellImageData_GetProperties, shimgdata/IShellImageData::GetProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.GetProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageData::GetProperties


## -description


Gets an <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> through which the properties of the image can be accessed.


## -parameters




### -param dwMode [in]

Type: <b>DWORD</b>

Not used, set to 0.


### -param ppPropSet [out]

Type: <b><a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>**</b>


          The address of a pointer to the <a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface.
        


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
 



