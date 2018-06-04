---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAppxFactory::CreatePackageWriter


## -description


Creates a write-only package object to which  files can be added.


## -parameters




### -param outputStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The output stream that receives the serialized package data. The stream must support at least the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> method.


### -param settings [in]

Type: <b><a href="https://msdn.microsoft.com/85874BCD-44EF-4442-96B8-F22AC4247DB4">APPX_PACKAGE_SETTINGS</a>*</b>

The settings for the production of this package.


### -param packageWriter [out, retval]

Type: <b><a href="https://msdn.microsoft.com/097B7451-9A54-4C39-8F83-16DB49691B42">IAppxPackageWriter</a>**</b>

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
The specified <b>hashMethod</b> member of the <a href="https://msdn.microsoft.com/85874BCD-44EF-4442-96B8-F22AC4247DB4">APPX_PACKAGE_SETTINGS</a> structure is not a valid hash algorithm URI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified <b>hashMethod</b> member of the <a href="https://msdn.microsoft.com/85874BCD-44EF-4442-96B8-F22AC4247DB4">APPX_PACKAGE_SETTINGS</a> structure is not a valid hash algorithm URI.

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



The implementation of an <a href="https://msdn.microsoft.com/097B7451-9A54-4C39-8F83-16DB49691B42">IAppxPackageWriter</a> is not guaranteed to write data to the output stream before the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> method is called on the writer object. No other thread should access <i>outputStream</i> until the writer returns from its <b>Close</b> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/FD677D75-50D5-4228-891F-73B5F40679B0">How to create an app  package</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>
 

 

