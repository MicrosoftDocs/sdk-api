---
UID: NF:appxpackaging.IAppxPackageReader.GetPayloadFile
title: IAppxPackageReader::GetPayloadFile
author: windows-sdk-content
description: Retrieves a payload file from the package.
old-location: appxpkg\iappxpackagereader_getpayloadfile.htm
old-project: appxpkg
ms.assetid: 83E6931D-405C-4A93-BE70-F505D484CB7F
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetPayloadFile, GetPayloadFile method [App packaging and management], GetPayloadFile method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetPayloadFile method, IAppxPackageReader.GetPayloadFile, IAppxPackageReader::GetPayloadFile, appxpackaging/IAppxPackageReader::GetPayloadFile, appxpkg.iappxpackagereader_getpayloadfile
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxPackageReader.GetPayloadFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageReader::GetPayloadFile


## -description


Retrieves a payload file from the package.


## -parameters




### -param fileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the payload file to be retrieved.


### -param file [out, retval]

Type: <b><a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>**</b>

The file object that corresponds to <i>fileName</i>.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
There is no payload file with the specified file name.

</td>
</tr>
</table>
 




## -remarks



The specified <i>fileName</i> must include the path relative to the package root directory. 




## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>



<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>



<a href="https://msdn.microsoft.com/8CCF9135-308F-4BDC-A67F-1E3ED2ACF565">IAppxPackageReader::GetFootprintFile</a>



<a href="https://msdn.microsoft.com/20883A4E-BE7B-4312-978A-3BF9362CA6DA">IAppxPackageReader::GetPayloadFiles</a>
 

 

