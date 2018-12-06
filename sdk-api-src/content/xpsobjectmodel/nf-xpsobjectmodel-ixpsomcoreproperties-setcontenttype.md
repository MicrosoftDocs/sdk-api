---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetContentType
title: IXpsOMCoreProperties::SetContentType
author: windows-sdk-content
description: Sets the contentType property.
old-location: xps\ixpsomcoreproperties_setcontenttype.htm
tech.root: printdocs
ms.assetid: 97ddb1a2-67b2-4891-86b6-bdd38e609229
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetContentType method, IXpsOMCoreProperties.SetContentType, IXpsOMCoreProperties::SetContentType, SetContentType, SetContentType method [XPS Documents and Packaging], SetContentType method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcontenttype, xpsobjectmodel/IXpsOMCoreProperties::SetContentType
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMCoreProperties.SetContentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCoreProperties::SetContentType


## -description


Sets the <b>contentType</b> property.


## -parameters




### -param contentType [in]

The string to be written to the <b>contentType</b> property. A <b>NULL</b> pointer clears the <b>contentType</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>contentType</b> property contains the type of content that is being represented, which is generally defined by a
specific use and intended audience. Examples of <b>contentType</b>  values include <b>Whitepaper</b>, <b>Security Bulletin</b>, and <b>Exam</b>.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

