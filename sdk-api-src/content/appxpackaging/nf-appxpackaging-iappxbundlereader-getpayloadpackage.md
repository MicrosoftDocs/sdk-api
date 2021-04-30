---
UID: NF:appxpackaging.IAppxBundleReader.GetPayloadPackage
title: IAppxBundleReader::GetPayloadPackage (appxpackaging.h)
description: Retrieves an appx file object for the payload package with the specified file name.
helpviewer_keywords: ["GetPayloadPackage","GetPayloadPackage method [App packaging and management]","GetPayloadPackage method [App packaging and management]","IAppxBundleReader interface","IAppxBundleReader interface [App packaging and management]","GetPayloadPackage method","IAppxBundleReader.GetPayloadPackage","IAppxBundleReader::GetPayloadPackage","appxpackaging/IAppxBundleReader::GetPayloadPackage","appxpkg.iappxbundlereader_getpayloadpackage"]
old-location: appxpkg\iappxbundlereader_getpayloadpackage.htm
tech.root: appxpkg
ms.assetid: 6ACAB26C-22FC-45D7-9F6A-98B56B615DCA
ms.date: 12/05/2018
ms.keywords: GetPayloadPackage, GetPayloadPackage method [App packaging and management], GetPayloadPackage method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetPayloadPackage method, IAppxBundleReader.GetPayloadPackage, IAppxBundleReader::GetPayloadPackage, appxpackaging/IAppxBundleReader::GetPayloadPackage, appxpkg.iappxbundlereader_getpayloadpackage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxBundleReader::GetPayloadPackage
 - appxpackaging/IAppxBundleReader::GetPayloadPackage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleReader.GetPayloadPackage
---

# IAppxBundleReader::GetPayloadPackage


## -description

Retrieves an appx file object for the payload package with the specified file name.

## -parameters

### -param fileName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the payload file to be retrieved.

### -param payloadPackage [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>**</b>

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

You can pass the file object’s stream into <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createpackagereader">IAppxFactory::CreatePackageReader</a> to get a package reader object over the appx file.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlereader">IAppxBundleReader</a>