---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetSubject
title: IXpsOMCoreProperties::SetSubject (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the subject property.
old-location: xps\ixpsomcoreproperties_setsubject.htm
tech.root: printdocs
ms.assetid: aa194dd0-3293-4c09-84ae-516478862f4c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetSubject method, IXpsOMCoreProperties.SetSubject, IXpsOMCoreProperties::SetSubject, SetSubject, SetSubject method [XPS Documents and Packaging], SetSubject method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setsubject, xpsobjectmodel/IXpsOMCoreProperties::SetSubject
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMCoreProperties.SetSubject"
dev_langs:
 - c++
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
 - IXpsOMCoreProperties.SetSubject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::SetSubject


## -description


Sets the <b>subject</b> property.


## -parameters




### -param subject [in]

The string to be written to the <b>subject</b> property. A <b>NULL</b> pointer clears the <b>subject</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>subject</b> property contains the topic of the resource content.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

