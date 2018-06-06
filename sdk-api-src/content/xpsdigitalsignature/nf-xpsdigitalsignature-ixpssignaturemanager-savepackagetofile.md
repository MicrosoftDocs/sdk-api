---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.SavePackageToFile
title: IXpsSignatureManager::SavePackageToFile
author: windows-sdk-content
description: Saves the XPS package to a file.
old-location: xps\ixpssignaturemanager_savepackagetofile.htm
old-project: printdocs
ms.assetid: 954d8eb1-8680-410b-909b-da7a6572c0f3
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],SavePackageToFile method, IXpsSignatureManager.SavePackageToFile, IXpsSignatureManager::SavePackageToFile, SavePackageToFile, SavePackageToFile method [XPS Documents and Packaging], SavePackageToFile method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_savepackagetofile, xpsdigitalsignature/IXpsSignatureManager::SavePackageToFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.SavePackageToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureManager::SavePackageToFile


## -description


Saves the XPS package to a file.


## -parameters




### -param fileName [in]

The name of the file where the XPS package is to be created and saved.


### -param securityAttributes [in]

The <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure,  which contains two separate but related data members:

<ul>
<li><b>lpSecurityDescriptor</b>, an optional security descriptor.</li>
<li><b>bInheritHandle</b>,  a Boolean value that determines whether the returned handle can be inherited by child processes.</li>
</ul>
If the <b>lpSecurityDescriptor</b> member of the structure is <b>NULL</b>, the file or device that is associated with the returned handle is assigned a default security descriptor.

For more information about this parameter, see <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


### -param flagsAndAttributes [in]

The file or device attributes and flags that will be used in file creation. For more information about this parameter, see the description of the <i>dwFlagsAndAttributes</i> parameter in <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


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
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>
 




## -remarks



If this method returns an <b>HRESULT</b> value that is not in the list of return values for this method, the signature manager should be released and recreated.




## -see-also




<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

