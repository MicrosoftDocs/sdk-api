---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAppxBundleReader::GetFootprintFile


## -description


Retrieves the specified type of footprint file from the bundle.


## -parameters




### -param fileType [in]

Type: <b><a href="https://msdn.microsoft.com/1BC2B15B-9DF3-48D8-B7BE-BEC1E5D7E6E3">APPX_BUNDLE_FOOTPRINT_FILE_TYPE</a></b>

The type of footprint file to be retrieved.


### -param footprintFile [out, retval]

Type: <b><a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>**</b>

The file object that corresponds to the footprint file of <i>fileType</i>.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>fileType</i> parameter is not a valid value in the <a href="https://msdn.microsoft.com/1BC2B15B-9DF3-48D8-B7BE-BEC1E5D7E6E3">APPX_BUNDLE_FOOTPRINT_FILE_TYPE</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The bundle doesn't contain a footprint file of the specified type.


<a href="https://msdn.microsoft.com/BD60CD3E-2C08-4B97-B311-00C0EEBEF752">GetFootprintFile</a> can return this error for the <a href="appx_bundle_footprint_file_type.htm">APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE</a> type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664">IAppxBundleReader</a>
 

 

