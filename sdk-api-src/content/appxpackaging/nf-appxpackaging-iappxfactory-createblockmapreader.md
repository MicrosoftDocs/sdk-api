---
UID: NF:appxpackaging.IAppxFactory.CreateBlockMapReader
title: IAppxFactory::CreateBlockMapReader
author: windows-sdk-content
description: Creates a read-only block map object model from contents provided by an IStream.
old-location: appxpkg\iappxfactory_createblockmapreader.htm
tech.root: appxpkg
ms.assetid: B4A310F0-4276-49AA-9ABF-A98F41E8F87F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBlockMapReader, CreateBlockMapReader method [App packaging and management], CreateBlockMapReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreateBlockMapReader method, IAppxFactory.CreateBlockMapReader, IAppxFactory::CreateBlockMapReader, appxpackaging/IAppxFactory::CreateBlockMapReader, appxpkg.iappxfactory_createblockmapreader
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
 - IAppxFactory.CreateBlockMapReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxFactory::CreateBlockMapReader


## -description


Creates a read-only block map object model from contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


## -parameters




### -param inputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream that delivers the block map XML for reading. The stream must support <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">Read</a>, <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param blockMapReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>**</b>

The block map reader.


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
<dt><b>APPX_E_INVALID_BLOCKMAP</b></dt>
</dl>
</td>
<td width="60%">
The <i>inputStream</i> does not contain syntactically valid XML for the block map.

</td>
</tr>
</table>
 




## -remarks



Use the  <b>CreateBlockMapReader</b> method to read a block map outside of an app package.  The <i>blockMapReader</i> provides access to all data elements and attributes in the block map XML. 




## -see-also




<a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>



<a href="https://msdn.microsoft.com/BCC39D9C-4AF9-4CFD-AC66-4B79F9F25BDC">IAppxFactory::CreateValidatedBlockMapReader</a>
 

 

