---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetRevision
title: IXpsOMCoreProperties::SetRevision (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the revision property.
old-location: xps\ixpsomcoreproperties_setrevision.htm
tech.root: printdocs
ms.assetid: 7e2ef3b4-64dd-402e-a282-0ed01e588337
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetRevision method, IXpsOMCoreProperties.SetRevision, IXpsOMCoreProperties::SetRevision, SetRevision, SetRevision method [XPS Documents and Packaging], SetRevision method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setrevision, xpsobjectmodel/IXpsOMCoreProperties::SetRevision
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMCoreProperties.SetRevision"
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
 - IXpsOMCoreProperties.SetRevision
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::SetRevision


## -description


Sets the <b>revision</b> property.


## -parameters




### -param revision [in]

The string to be written to the <b>revision</b> property. A <b>NULL</b> pointer clears the <b>revision</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>revision</b> property contains the revision number of the resource.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

