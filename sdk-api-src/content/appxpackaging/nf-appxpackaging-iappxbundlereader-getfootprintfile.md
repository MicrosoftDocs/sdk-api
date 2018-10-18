---
UID: NF:appxpackaging.IAppxBundleReader.GetFootprintFile
title: IAppxBundleReader::GetFootprintFile
author: windows-sdk-content
description: Retrieves the specified type of footprint file from the bundle.
old-location: appxpkg\iappxbundlereader_getfootprintfile.htm
tech.root: appxpkg
ms.assetid: BD60CD3E-2C08-4B97-B311-00C0EEBEF752
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetFootprintFile, GetFootprintFile method [App packaging and management], GetFootprintFile method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetFootprintFile method, IAppxBundleReader.GetFootprintFile, IAppxBundleReader::GetFootprintFile, appxpackaging/IAppxBundleReader::GetFootprintFile, appxpkg.iappxbundlereader_getfootprintfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleReader.GetFootprintFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


<a href="https://msdn.microsoft.com/BD60CD3E-2C08-4B97-B311-00C0EEBEF752">GetFootprintFile</a> can return this error for the <a href="https://msdn.microsoft.com/en-us/library/Dn280275(v=VS.85).aspx">APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE</a> type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664">IAppxBundleReader</a>
 

 

