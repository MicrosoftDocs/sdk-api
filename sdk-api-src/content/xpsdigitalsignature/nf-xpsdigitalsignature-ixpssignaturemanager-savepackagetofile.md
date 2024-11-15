---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.SavePackageToFile
title: IXpsSignatureManager::SavePackageToFile (xpsdigitalsignature.h)
description: Saves the XPS package to a file.
helpviewer_keywords: ["IXpsSignatureManager interface [XPS Documents and Packaging]","SavePackageToFile method","IXpsSignatureManager.SavePackageToFile","IXpsSignatureManager::SavePackageToFile","SavePackageToFile","SavePackageToFile method [XPS Documents and Packaging]","SavePackageToFile method [XPS Documents and Packaging]","IXpsSignatureManager interface","xps.ixpssignaturemanager_savepackagetofile","xpsdigitalsignature/IXpsSignatureManager::SavePackageToFile"]
old-location: xps\ixpssignaturemanager_savepackagetofile.htm
tech.root: xps
ms.assetid: 954d8eb1-8680-410b-909b-da7a6572c0f3
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],SavePackageToFile method, IXpsSignatureManager.SavePackageToFile, IXpsSignatureManager::SavePackageToFile, SavePackageToFile, SavePackageToFile method [XPS Documents and Packaging], SavePackageToFile method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_savepackagetofile, xpsdigitalsignature/IXpsSignatureManager::SavePackageToFile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsSignatureManager::SavePackageToFile
 - xpsdigitalsignature/IXpsSignatureManager::SavePackageToFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.SavePackageToFile
---

# IXpsSignatureManager::SavePackageToFile


## -description

Saves the XPS package to a file.

## -parameters

### -param fileName [in]

The name of the file where the XPS package is to be created and saved.

### -param securityAttributes [in]

The <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure,  which contains two separate but related data members:

<ul>
<li><b>lpSecurityDescriptor</b>, an optional security descriptor.</li>
<li><b>bInheritHandle</b>,  a Boolean value that determines whether the returned handle can be inherited by child processes.</li>
</ul>
If the <b>lpSecurityDescriptor</b> member of the structure is <b>NULL</b>, the file or device that is associated with the returned handle is assigned a default security descriptor.

For more information about this parameter, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param flagsAndAttributes [in]

The file or device attributes and flags that will be used in file creation. For more information about this parameter, see the description of the <i>dwFlagsAndAttributes</i> parameter in <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>