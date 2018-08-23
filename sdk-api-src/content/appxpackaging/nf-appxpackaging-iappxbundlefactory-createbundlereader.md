---
UID: NF:appxpackaging.IAppxBundleFactory.CreateBundleReader
title: IAppxBundleFactory::CreateBundleReader
author: windows-sdk-content
description: Creates a read-only bundle object that reads its contents from an IStream object.
old-location: appxpkg\iappxbundlefactory_createbundlereader.htm
old-project: appxpkg
ms.assetid: 3D9F7A0A-EF6A-4C99-B9A0-C618138DB5ED
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: CreateBundleReader, CreateBundleReader method [App packaging and management], CreateBundleReader method [App packaging and management],IAppxBundleFactory interface, IAppxBundleFactory interface [App packaging and management],CreateBundleReader method, IAppxBundleFactory.CreateBundleReader, IAppxBundleFactory::CreateBundleReader, appxpackaging/IAppxBundleFactory::CreateBundleReader, appxpkg.iappxbundlefactory_createbundlereader
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
 - IAppxBundleFactory.CreateBundleReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleFactory::CreateBundleReader


## -description


Creates a read-only bundle object that reads its contents from an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 


## -parameters




### -param inputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The input stream that delivers the content of the package for reading. The stream must support <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">Read</a>, <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param bundleReader [out, retval]

Type: <b>IAppxBundleReader**</b>

A  bundle  reader.


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
<dt><b>APPX_E_INTERLEAVING_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
The ZIP file delivered by <i>inputStream</i> is an interleaved OPC package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_RELATIONSHIPS_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
The OPC package delivered by <i>inputStream</i> contains OPC package/part relationships.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_MISSING_REQUIRED_FILE</b></dt>
</dl>
</td>
<td width="60%">
The OPC package delivered by <i>inputStream</i> does not have a manifest, or a block map, or a signature file when a CI catalog is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The bundle manifest is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/33A320BD-7B68-4C42-A776-25CC744C6652">IAppxBundleFactory</a>
 

 

