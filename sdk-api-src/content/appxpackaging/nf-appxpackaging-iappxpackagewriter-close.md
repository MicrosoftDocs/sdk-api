---
UID: NF:appxpackaging.IAppxPackageWriter.Close
title: IAppxPackageWriter::Close method
author: windows-driver-content
description: Writes footprint files at the end of the app package, and closes the package writer object's output stream.
old-location: appxpkg\iappxpackagewriter_close.htm
old-project: appxpkg
ms.assetid: 294625B2-1141-44EE-A769-365C3B37EBD9
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: Close method [App packaging and management], Close method [App packaging and management], IAppxPackageWriter interface, Close,IAppxPackageWriter.Close, IAppxPackageWriter, IAppxPackageWriter interface [App packaging and management], Close method, IAppxPackageWriter::Close, appxpackaging/IAppxPackageWriter::Close, appxpkg.iappxpackagewriter_close
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxPackageWriter.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageWriter::Close method


## -description


Writes footprint files at the end of the app package, and closes the package writer object's output stream.


## -parameters




### -param manifest [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream that provides the contents of the manifest for the package. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


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
<dt><b>E_NOT_VALID_STATE </b></dt>
</dl>
</td>
<td width="60%">
The writer is closed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The input stream contains a manifest that is not valid. 

</td>
</tr>
</table>
 




## -remarks



The <b>Close</b> method should be called only after all payload files have been added to the package. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/FD677D75-50D5-4228-891F-73B5F40679B0">How to create an app  package</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/097B7451-9A54-4C39-8F83-16DB49691B42">IAppxPackageWriter</a>
 

 

