---
UID: NF:xpsobjectmodel_1.IXpsOMRemoteDictionaryResource1.Write1
title: IXpsOMRemoteDictionaryResource1::Write1
author: windows-driver-content
description: Serializes the remote dictionary resource to a stream.
old-location: xps\ixpsomremotedictionaryresource1_write1.htm
old-project: printdocs
ms.assetid: 5C5C2DC9-1F03-44F9-9466-7AFD1BD5D098
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMRemoteDictionaryResource1 interface [XPS Documents and Packaging],Write1 method, IXpsOMRemoteDictionaryResource1.Write1, IXpsOMRemoteDictionaryResource1::Write1, Write1, Write1 method [XPS Documents and Packaging], Write1 method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResource1 interface, xps.ixpsomremotedictionaryresource1_write1, xpsobjectmodel_1/IXpsOMRemoteDictionaryResource1::Write1
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
-	IXpsOMRemoteDictionaryResource1.Write1
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRemoteDictionaryResource1::Write1


## -description


Serializes the remote dictionary resource to a stream.


## -parameters




### -param stream [in]

The stream that receives the serialized contents of the dictionary.


### -param documentType [in]

The XPS data format to write to outputStream. The value of this parameter cannot be <b>XPS_DOCUMENT_TYPE_UNSPECIFIED</b>.


## -returns



The method returns an <b>HRESULT</b>.

For information about  XPS document API return values, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/4B8DEDC7-4D7A-408F-9B2B-67B6FC87372F">IXpsOMRemoteDictionaryResource1</a>
 

 

