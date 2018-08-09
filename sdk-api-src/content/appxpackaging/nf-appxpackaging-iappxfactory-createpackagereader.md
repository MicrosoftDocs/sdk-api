---
UID: NF:appxpackaging.IAppxFactory.CreatePackageReader
title: IAppxFactory::CreatePackageReader
author: windows-sdk-content
description: Creates a read-only package reader from the contents provided by an IStream. This method does not validate the digital signature.
old-location: appxpkg\iappxfactory_createpackagereader.htm
old-project: appxpkg
ms.assetid: 60C9781F-A1EE-4EAA-9CD5-32692F3E063D
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CreatePackageReader, CreatePackageReader method [App packaging and management], CreatePackageReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreatePackageReader method, IAppxFactory.CreatePackageReader, IAppxFactory::CreatePackageReader, appxpackaging/IAppxFactory::CreatePackageReader, appxpkg.iappxfactory_createpackagereader
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
 - IAppxFactory.CreatePackageReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFactory::CreatePackageReader


## -description


Creates a read-only package reader from the contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>. This method does not validate the <a href="https://msdn.microsoft.com/DD88F9D9-E866-4941-8D04-B6959AC2F1CF">digital signature</a>.


## -parameters




### -param inputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The input stream that delivers the content of the package for reading. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param packageReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>**</b>

A  package  reader.


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
The package manifest is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INVALID_BLOCKMAP</b></dt>
</dl>
</td>
<td width="60%">
The package block map is not valid, the list of files in the ZIP central directory does not match the list of files in the block map, or the size of files listed in the ZIP central directory does not match the file and block sizes listed in the block map.

</td>
</tr>
</table>
 




## -remarks



The  <b>CreatePackageReader</b> method immediately retrieves footprint elements of the app package through the stream and validates their content.  This method succeeds only if the OPC package and all footprint elements (including ZIP central directory, manifest, [Content_Types].xml, and block map) are valid.  


#### Examples

For an example, see <a href="https://msdn.microsoft.com/72C368F9-2EBA-4930-81CF-9B85717CC0AA">Quickstart: Extract app package contents</a> and <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>
 

 

