---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePackageWriterOnStream1
title: IXpsOMObjectFactory1::CreatePackageWriterOnStream1
author: windows-driver-content
description: Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type.
old-location: xps\ixpsomobjectfactory1_createpackagewriteronstream1.htm
old-project: printdocs
ms.assetid: ce948f17-689a-4430-8152-20fbecaf6ee9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreatePackageWriterOnStream1, CreatePackageWriterOnStream1 method [XPS Documents and Packaging], CreatePackageWriterOnStream1 method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, FALSE, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],CreatePackageWriterOnStream1 method, IXpsOMObjectFactory1.CreatePackageWriterOnStream1, IXpsOMObjectFactory1::CreatePackageWriterOnStream1, TRUE, xps.ixpsomobjectfactory1_createpackagewriteronstream1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnStream1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_DOCUMENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	none
-	none.dll
api_name:
-	IXpsOMObjectFactory1.CreatePackageWriterOnStream1
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory1::CreatePackageWriterOnStream1


## -description


Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type. 


## -parameters




### -param outputStream

[in] The stream to be used for writing.


### -param optimizeMarkupSize

A Boolean value that  indicates whether the document markup will be optimized for size when the document is written to the stream.

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
When writing to the stream, the package writer will attempt to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
When writing to the package, the package writer will not attempt any optimization.

</td>
</tr>
</table>
 


### -param interleaving

[in] Specifies whether the content of the XPS OM will be interleaved when it is written to the stream.


### -param documentSequencePartName

[in] The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.


### -param coreProperties

[in] The <a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a> interface that contains the core document properties to be given to the new file. This parameter can be set to <b>NULL</b>.


### -param packageThumbnail

[in] The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the thumbnail image to be assigned to the new file.  This parameter can be set to <b>NULL</b>.


### -param documentSequencePrintTicket

[in] The <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file.  This parameter can be set to <b>NULL</b>.


### -param discardControlPartName

[in] The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the name of the discard control part.  This parameter can be set to <b>NULL</b>.


### -param documentType

[in] The document type of the package writer. The value of this parameter cannot be XPS_DOCUMENT_TYPE_UNSPECIFIED.


### -param packageWriter

[out, retval]    A pointer to the new <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface created by this method.


## -returns



Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded and packageWriter was set correctly. 

E_INVALIDARG: The document type was not a valid XPS document format. 




## -remarks



Use this method to produce a package writer for either an MSXPS document or an OpenXPS document. <a href="https://msdn.microsoft.com/77f432e3-7b6a-426f-8673-06dbf3038443">CreatePackageWriterOnStream</a>,  released in Windows 7, only creates XPS document files in the MSXPS format.




## -see-also




<a href="https://msdn.microsoft.com/f013e59d-83ae-453f-9cc5-9a8230729128">IXpsOMObjectFactory1</a>
 

 

