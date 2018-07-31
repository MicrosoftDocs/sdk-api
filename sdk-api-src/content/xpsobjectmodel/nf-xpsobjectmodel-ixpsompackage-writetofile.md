---
UID: NF:xpsobjectmodel.IXpsOMPackage.WriteToFile
title: IXpsOMPackage::WriteToFile
author: windows-sdk-content
description: Writes the XPS package to a specified file.
old-location: xps\ixpsompackage_writetofile.htm
old-project: printdocs
ms.assetid: 89accde7-989e-4a87-b96e-e47cc6c6954a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FALSE, IXpsOMPackage interface [XPS Documents and Packaging],WriteToFile method, IXpsOMPackage.WriteToFile, IXpsOMPackage::WriteToFile, TRUE, WriteToFile, WriteToFile method [XPS Documents and Packaging], WriteToFile method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_writetofile, xpsobjectmodel/IXpsOMPackage::WriteToFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPackage.WriteToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPackage::WriteToFile


## -description


Writes the XPS package to a specified file.


## -parameters




### -param fileName [in]

The name of the file to be created. This parameter must not be <b>NULL</b>.


### -param securityAttributes [in]

The <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure, which contains two distinct but related data members:

<ul>
<li><b>lpSecurityDescriptor</b>: an optional security descriptor</li>
<li><b>bInheritHandle</b>:  a Boolean value that determines whether the returned handle can be inherited by child processes</li>
</ul>
If  <b>lpSecurityDescriptor</b> is <b>NULL</b>, the file or device that is associated with the returned handle will be assigned a default security descriptor. 

For more information about the <i>securityAttributes</i> parameter, refer to <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


### -param flagsAndAttributes [in]

Specifies the settings and attributes of the file to be  created. For most files, a value of <b>FILE_ATTRIBUTE_NORMAL</b> can be used. 


For more information about the <i>flagsAndAttributes</i> parameter, refer to <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


### -param optimizeMarkupSize [in]

A Boolean value that  indicates whether the document markup is to be optimized for size when it is written to the file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will attempt to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will not attempt any optimization.

</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
</table>
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



The <i>optimizeMarkupSize</i> value determines whether the markup inside the individual document parts is to be optimized. It has  no effect on how the parts are interleaved.

<div class="alert"><b>Note</b>  Writing an XPS OM to a file does not automatically create a thumbnail for the XPS document. To create a thumbnail of the XPS document, use the <a href="https://msdn.microsoft.com/cac794c0-bea2-417e-880f-15838f718ba7">IXpsOMThumbnailGenerator</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

