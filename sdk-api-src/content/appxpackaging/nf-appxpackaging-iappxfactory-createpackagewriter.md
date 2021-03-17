---
UID: NF:appxpackaging.IAppxFactory.CreatePackageWriter
title: IAppxFactory::CreatePackageWriter (appxpackaging.h)
description: Creates a write-only package object to which files can be added.
helpviewer_keywords: ["CreatePackageWriter","CreatePackageWriter method [App packaging and management]","CreatePackageWriter method [App packaging and management]","IAppxFactory interface","IAppxFactory interface [App packaging and management]","CreatePackageWriter method","IAppxFactory.CreatePackageWriter","IAppxFactory::CreatePackageWriter","appxpackaging/IAppxFactory::CreatePackageWriter","appxpkg.iappxfactory_createpackagewriter"]
old-location: appxpkg\iappxfactory_createpackagewriter.htm
tech.root: appxpkg
ms.assetid: 10E9250E-7A64-4FB0-ACB9-10CB144A0FBE
ms.date: 12/05/2018
ms.keywords: CreatePackageWriter, CreatePackageWriter method [App packaging and management], CreatePackageWriter method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreatePackageWriter method, IAppxFactory.CreatePackageWriter, IAppxFactory::CreatePackageWriter, appxpackaging/IAppxFactory::CreatePackageWriter, appxpkg.iappxfactory_createpackagewriter
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFactory::CreatePackageWriter
 - appxpackaging/IAppxFactory::CreatePackageWriter
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
 - IAppxFactory.CreatePackageWriter
---

# IAppxFactory::CreatePackageWriter


## -description

Creates a write-only package object to which  files can be added.

## -parameters

### -param outputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The output stream that receives the serialized package data. The stream must support at least the  <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">Write</a> method.

### -param settings [in]

Type: <b><a href="/windows/desktop/api/appxpackaging/ns-appxpackaging-appx_package_settings">APPX_PACKAGE_SETTINGS</a>*</b>

The settings for the production of this package.

### -param packageWriter [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter">IAppxPackageWriter</a>**</b>

The package writer created by this method.

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
The specified <b>hashMethod</b> member of the <a href="/windows/desktop/api/appxpackaging/ns-appxpackaging-appx_package_settings">APPX_PACKAGE_SETTINGS</a> structure is not a valid hash algorithm URI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified <b>hashMethod</b> member of the <a href="/windows/desktop/api/appxpackaging/ns-appxpackaging-appx_package_settings">APPX_PACKAGE_SETTINGS</a> structure is not a valid hash algorithm URI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The hash value is <a href="http://www.w3.org/2000/09/xmldsig">SHA1</a>.

</td>
</tr>
</table>

## -remarks

The implementation of an <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagewriter">IAppxPackageWriter</a> is not guaranteed to write data to the output stream before the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagewriter-close">Close</a> method is called on the writer object. No other thread should access <i>outputStream</i> until the writer returns from its <b>Close</b> method.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-create-a-package">How to create an app  package</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a>