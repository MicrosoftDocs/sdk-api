---
UID: NF:appxpackaging.IAppxPackageReader.GetFootprintFile
title: IAppxPackageReader::GetFootprintFile
author: windows-sdk-content
description: Retrieves a footprint file from the package.
old-location: appxpkg\iappxpackagereader_getfootprintfile.htm
old-project: appxpkg
ms.assetid: 8CCF9135-308F-4BDC-A67F-1E3ED2ACF565
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetFootprintFile, GetFootprintFile method [App packaging and management], GetFootprintFile method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetFootprintFile method, IAppxPackageReader.GetFootprintFile, IAppxPackageReader::GetFootprintFile, appxpackaging/IAppxPackageReader::GetFootprintFile, appxpkg.iappxpackagereader_getfootprintfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageReader.GetFootprintFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageReader::GetFootprintFile


## -description


Retrieves a footprint file from the package.


## -parameters




### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/AF158108-06E5-45D5-BD64-DA3CEFFB88F0">APPX_FOOTPRINT_FILE_TYPE</a></b>

The type of footprint file to be retrieved.


### -param file [out, retval]

Type: <b><a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>**</b>

The file object that corresponds to the footprint file of <i>type</i>.


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
The <i>type</i> parameter is not a member of the <a href="https://msdn.microsoft.com/AF158108-06E5-45D5-BD64-DA3CEFFB88F0">APPX_FOOTPRINT_FILE_TYPE</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The package does not contain a footprint file of the specified type.


<a href="https://msdn.microsoft.com/8CCF9135-308F-4BDC-A67F-1E3ED2ACF565">GetFootprintFile</a> can return this error for <a href="appx_footprint_file_type.htm">APPX_FOOTPRINT_FILE_TYPE_SIGNATURE</a> and <a href="appx_footprint_file_type.htm">APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY</a> types.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>



<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>



<a href="https://msdn.microsoft.com/83E6931D-405C-4A93-BE70-F505D484CB7F">IAppxPackageReader::GetPayloadFile</a>



<a href="https://msdn.microsoft.com/20883A4E-BE7B-4312-978A-3BF9362CA6DA">IAppxPackageReader::GetPayloadFiles</a>
 

 

