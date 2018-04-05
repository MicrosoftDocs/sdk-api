---
UID: NF:appxpackaging.IAppxPackageWriter.AddPayloadFile
title: IAppxPackageWriter::AddPayloadFile method
author: windows-driver-content
description: Adds a new payload file to the app package.
old-location: appxpkg\iappxpackagewriter_addpayloadfile.htm
old-project: appxpkg
ms.assetid: 2BFC725A-CD56-46CA-983A-FD1BFB6CB474
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: AddPayloadFile method [App packaging and management], AddPayloadFile method [App packaging and management], IAppxPackageWriter interface, AddPayloadFile,IAppxPackageWriter.AddPayloadFile, IAppxPackageWriter, IAppxPackageWriter interface [App packaging and management], AddPayloadFile method, IAppxPackageWriter::AddPayloadFile, appxpackaging/IAppxPackageWriter::AddPayloadFile, appxpkg.iappxpackagewriter_addpayloadfile
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
-	IAppxPackageWriter.AddPayloadFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageWriter::AddPayloadFile method


## -description


Adds a new payload file to the app package.


## -parameters




### -param fileName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the payload file. The file name path must be relative to the root of the package.


### -param contentType [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>


            The string specifying the <a href="http://go.microsoft.com/fwlink/p/?linkid=143979">content type</a> of  <i>fileName</i>.
          


### -param compressionOption [in]

Type: <b><a href="https://msdn.microsoft.com/C4FEE4DA-1097-4870-BB43-A910E20BCBD6">APPX_COMPRESSION_OPTION</a></b>


            The type of compression to use  to store <i>fileName</i> in the package. 


### -param inputStream [in]

Type: <b>IStream*</b>


            An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> providing the contents of <i>fileName</i>.
          The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. Error OPC codes, in addition to  OPC_E_DUPLICATE_PART may result. If the method fails, the package writer will close in a failed state and can't be used any more.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The compression option specified by <i>compressionOption</i> is not one of the values of the <a href="https://msdn.microsoft.com/C4FEE4DA-1097-4870-BB43-A910E20BCBD6">APPX_COMPRESSION_OPTION</a> enumeration.

</td>
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
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_NAME)</b></dt>
</dl>
</td>
<td width="60%">
The file name specified is not a valid file name or is a reserved name for a footprint file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_PART</b></dt>
</dl>
</td>
<td width="60%">
The file name specified is already in use in the package. 

</td>
</tr>
</table>
 




## -remarks



When the <b>AddPayloadFile</b> method succeeds the contents of the specified <i>fileName</i> are written to the package and a corresponding entry is made in the package block map.


<div class="alert"><b>Note</b>  Files with the following reserved filenames cannnot be added to the package using the <b>AddPayloadFile</b> method:

    <b>\AppxManifest.xml</b>, 
    <b>\AppxBlockMap.xml</b>, <b>\AppxStreamMap.xml
    </b>, and <b>
    \AppxSignature.p7x

</b>.  Also, files with the following reserved folder prefixes cannnot be added to the package using the <b>AddPayloadFile</b> method:

    <b>\AppxMetadata\</b>
     and <b>\Microsoft.System.Package.Metadata\</b>. 

</div>
<div> </div>





#### Examples

For an example, see <a href="https://msdn.microsoft.com/FD677D75-50D5-4228-891F-73B5F40679B0">How to create an app  package</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/C4FEE4DA-1097-4870-BB43-A910E20BCBD6">APPX_COMPRESSION_OPTION</a>



<a href="https://msdn.microsoft.com/097B7451-9A54-4C39-8F83-16DB49691B42">IAppxPackageWriter</a>
 

 

