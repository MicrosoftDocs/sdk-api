---
UID: NF:appxpackaging.IAppxBundleFactory.CreateBundleManifestReader
title: IAppxBundleFactory::CreateBundleManifestReader
author: windows-driver-content
description: Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml.
old-location: appxpkg\iappxbundlefactory_createbundlemanifestreader.htm
old-project: appxpkg
ms.assetid: 8D537830-A8AA-4652-B6F2-F7A545B8877E
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CreateBundleManifestReader, CreateBundleManifestReader method [App packaging and management], CreateBundleManifestReader method [App packaging and management],IAppxBundleFactory interface, IAppxBundleFactory interface [App packaging and management],CreateBundleManifestReader method, IAppxBundleFactory.CreateBundleManifestReader, IAppxBundleFactory::CreateBundleManifestReader, appxpackaging/IAppxBundleFactory::CreateBundleManifestReader, appxpkg.iappxbundlefactory_createbundlemanifestreader
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleFactory.CreateBundleManifestReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleFactory::CreateBundleManifestReader


## -description


Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml.


## -parameters




### -param inputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The input stream  that delivers the manifest XML for reading. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param manifestReader [out, retval]

Type: <b>IAppxBundleManifestReader**</b>

The manifest reader.


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
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>inputStream</i> does not contain syntactically valid XML for the manifest.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/33A320BD-7B68-4C42-A776-25CC744C6652">IAppxBundleFactory</a>
 

 

