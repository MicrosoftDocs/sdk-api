---
UID: NF:appxpackaging.IAppxBundleReader.GetPayloadPackage
title: IAppxBundleReader::GetPayloadPackage
author: windows-sdk-content
description: Retrieves an appx file object for the payload package with the specified file name.
old-location: appxpkg\iappxbundlereader_getpayloadpackage.htm
old-project: appxpkg
ms.assetid: 6ACAB26C-22FC-45D7-9F6A-98B56B615DCA
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetPayloadPackage, GetPayloadPackage method [App packaging and management], GetPayloadPackage method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetPayloadPackage method, IAppxBundleReader.GetPayloadPackage, IAppxBundleReader::GetPayloadPackage, appxpackaging/IAppxBundleReader::GetPayloadPackage, appxpkg.iappxbundlereader_getpayloadpackage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
 - IAppxBundleReader.GetPayloadPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleReader::GetPayloadPackage


## -description


Retrieves an appx file object for the payload package with the specified file name.


## -parameters




### -param fileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the payload file to be retrieved.


### -param payloadPackage [out, retval]

Type: <b><a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>**</b>

The payload file object the that corresponds to <i>fileName</i>.


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



You can pass the file object’s stream into <a href="https://msdn.microsoft.com/60C9781F-A1EE-4EAA-9CD5-32692F3E063D">IAppxFactory::CreatePackageReader</a> to get a package reader object over the appx file. 




## -see-also




<a href="https://msdn.microsoft.com/3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664">IAppxBundleReader</a>
 

 

