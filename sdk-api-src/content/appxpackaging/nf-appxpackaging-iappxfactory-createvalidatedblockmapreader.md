---
UID: NF:appxpackaging.IAppxFactory.CreateValidatedBlockMapReader
title: IAppxFactory::CreateValidatedBlockMapReader
author: windows-sdk-content
description: Creates a read-only block map object model from contents provided by an IStream and a digital signature.
old-location: appxpkg\iappxfactory_createvalidatedblockmapreader.htm
old-project: appxpkg
ms.assetid: BCC39D9C-4AF9-4CFD-AC66-4B79F9F25BDC
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: CreateValidatedBlockMapReader, CreateValidatedBlockMapReader method [App packaging and management], CreateValidatedBlockMapReader method [App packaging and management],IAppxFactory interface, IAppxFactory interface [App packaging and management],CreateValidatedBlockMapReader method, IAppxFactory.CreateValidatedBlockMapReader, IAppxFactory::CreateValidatedBlockMapReader, appxpackaging/IAppxFactory::CreateValidatedBlockMapReader, appxpkg.iappxfactory_createvalidatedblockmapreader
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
 - IAppxFactory.CreateValidatedBlockMapReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFactory::CreateValidatedBlockMapReader


## -description


Creates a read-only block map object model from contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> and a digital signature.


## -parameters




### -param blockMapStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream that delivers block map XML for reading. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


### -param signatureFileName




### -param blockMapReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>**</b>

The block map reader.


#### - fileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The file that contains a digital signature used to validate the contents of the input stream.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those below. This method might return errors that are passed from the underlying validation APIs that are used.
For example, this method might return "Crypto and WinTrust error codes (0x8009xxxx, 0x800bxxxx) if the signature can't be read, is invalid, or doesn't match the content of <i>blockMapStream</i>.


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
The <i>blockMapStream</i> does not contain syntactically valid XML for the block map.

</td>
</tr>
</table>
 




## -remarks



This method is used when the block map exists alone, outside of an app package.  The block map object provides access to all data elements and attributes in the block map XML.

The <i>fileName</i> parameter should include the path of a package digital signature (.p7x) file on disk.  If this parameter is not <b>NULL</b>, this method will validate the format of the signature file and validate the contents of <i>blockMapStream</i> against the signature. 




## -see-also




<a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>



<a href="https://msdn.microsoft.com/B4A310F0-4276-49AA-9ABF-A98F41E8F87F">IAppxFactory::CreateBlockMapReader</a>
 

 

