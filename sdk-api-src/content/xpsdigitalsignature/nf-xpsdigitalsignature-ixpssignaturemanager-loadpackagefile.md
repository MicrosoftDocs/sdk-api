---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.LoadPackageFile
title: IXpsSignatureManager::LoadPackageFile
author: windows-sdk-content
description: Loads an existing XPS package from a file into the digital signature manager.
old-location: xps\ixpssignaturemanager_loadpackagefile.htm
tech.root: printdocs
ms.assetid: ecb33eee-4622-4a2e-bc24-7a77d16ef4a4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],LoadPackageFile method, IXpsSignatureManager.LoadPackageFile, IXpsSignatureManager::LoadPackageFile, LoadPackageFile, LoadPackageFile method [XPS Documents and Packaging], LoadPackageFile method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_loadpackagefile, xpsdigitalsignature/IXpsSignatureManager::LoadPackageFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.LoadPackageFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureManager::LoadPackageFile


## -description


Loads an existing XPS package from a file into the digital signature manager.


## -parameters




### -param fileName [in]

The file name of the XPS package to be loaded.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a> and  <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>fileName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_PACKAGE_ALREADY_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has already  been opened in the signature manager.

</td>
</tr>
</table>
 




## -remarks



 After the interface has been instantiated, the XPS package must be loaded by calling this method or <a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a> before
calling any other method in this interface.

After an XPS package has been loaded into an instance of <a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>, calling <b>LoadPackageFile</b> or <a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a> in the same instance will return an error.

After <b>LoadPackageFile</b> or <a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a> has been called, the same object cannot be reused for another XPS package file or stream. To load another XPS package, a new instance of   <a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a> must be instantiated.


<a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a> does not validate all content of the XPS package; it does not, for example, detect invalid markup in a FixedPage part.




## -see-also




<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

