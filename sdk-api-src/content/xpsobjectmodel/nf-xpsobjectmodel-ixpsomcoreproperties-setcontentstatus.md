---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetContentStatus
title: IXpsOMCoreProperties::SetContentStatus (xpsobjectmodel.h)
description: Sets the contentStatus property.
old-location: xps\ixpsomcoreproperties_setcontentstatus.htm
tech.root: printdocs
ms.assetid: f500407d-3eb4-4bf1-88ef-8f6bd2bcf472
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetContentStatus method, IXpsOMCoreProperties.SetContentStatus, IXpsOMCoreProperties::SetContentStatus, SetContentStatus, SetContentStatus method [XPS Documents and Packaging], SetContentStatus method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcontentstatus, xpsobjectmodel/IXpsOMCoreProperties::SetContentStatus
f1_keywords:
- xpsobjectmodel/IXpsOMCoreProperties.SetContentStatus
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
- IXpsOMCoreProperties.SetContentStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::SetContentStatus


## -description


Sets the <b>contentStatus</b> property.


## -parameters




### -param contentStatus [in]

The string to be written to the <b>contentStatus</b> property. A <b>NULL</b> pointer clears the <b>contentStatus</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>contentStatus</b> property contains the status of the content. Examples of <b>contentStatus</b> values include <b>Draft</b>, <b>Reviewed</b>, and <b>Final</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

