---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetKeywords
title: IXpsOMCoreProperties::SetKeywords (xpsobjectmodel.h)
description: Sets the keywords property.
helpviewer_keywords: ["IXpsOMCoreProperties interface [XPS Documents and Packaging]","SetKeywords method","IXpsOMCoreProperties.SetKeywords","IXpsOMCoreProperties::SetKeywords","SetKeywords","SetKeywords method [XPS Documents and Packaging]","SetKeywords method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","xps.ixpsomcoreproperties_setkeywords","xpsobjectmodel/IXpsOMCoreProperties::SetKeywords"]
old-location: xps\ixpsomcoreproperties_setkeywords.htm
tech.root: xps
ms.assetid: d96a85d2-dfbf-4589-9c3f-7505715ec6ce
ms.date: 12/05/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetKeywords method, IXpsOMCoreProperties.SetKeywords, IXpsOMCoreProperties::SetKeywords, SetKeywords, SetKeywords method [XPS Documents and Packaging], SetKeywords method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setkeywords, xpsobjectmodel/IXpsOMCoreProperties::SetKeywords
f1_keywords:
- xpsobjectmodel/IXpsOMCoreProperties.SetKeywords
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
- IXpsOMCoreProperties.SetKeywords
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::SetKeywords


## -description


Sets the <b>keywords</b> property.


## -parameters




### -param keywords [in]

The string that contains the keywords to be written to the <b>keywords</b> property. A <b>NULL</b> pointer clears the <b>keywords</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>keywords</b> property is a delimited set of keywords that are used to support searching and
indexing. It is typically a list of terms that are not
available elsewhere in the properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

