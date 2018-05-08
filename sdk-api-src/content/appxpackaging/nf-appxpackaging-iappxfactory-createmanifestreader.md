---
UID: NF:appxpackaging.IAppxFactory.CreateManifestReader
title: IAppxFactory::CreateManifestReader
author: windows-driver-content
description: Creates a read-only manifest object model from contents provided by an IStream.
old-location: appxpkg\iappxfactory_createmanifestreader.htm
old-project: appxpkg
ms.assetid: BF6C83FF-8CB1-47C0-84C3-E71059F0796E
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CreateManifestReader, CreateManifestReader method [App packaging and management], CreateManifestReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreateManifestReader method, IAppxFactory.CreateManifestReader, IAppxFactory::CreateManifestReader, appxpackaging/IAppxFactory::CreateManifestReader, appxpkg.iappxfactory_createmanifestreader
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxFactory.CreateManifestReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFactory::CreateManifestReader


## -description


Creates a read-only manifest object model from contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


## -parameters




### -param inputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The input stream  that delivers the manifest XML for reading. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param manifestReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>**</b>

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
 




## -remarks



Use <b>CreateManifestReader</b> to read a manifest outside of an app package.  This method validates the manifest XML. The <i>manifestReader</i> provides access to all data elements and attributes in the manifest XML. The manifest logs the location of manifest validation errors in the ETW event log for AppxPackaging. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>
 

 

