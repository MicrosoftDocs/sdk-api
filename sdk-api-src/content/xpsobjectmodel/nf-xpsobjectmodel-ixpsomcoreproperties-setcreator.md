---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetCreator
title: IXpsOMCoreProperties::SetCreator
author: windows-sdk-content
description: Sets the creator property.
old-location: xps\ixpsomcoreproperties_setcreator.htm
tech.root: printdocs
ms.assetid: 83dd62df-71e1-44a6-bf38-461b7e26e54e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetCreator method, IXpsOMCoreProperties.SetCreator, IXpsOMCoreProperties::SetCreator, SetCreator, SetCreator method [XPS Documents and Packaging], SetCreator method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setcreator, xpsobjectmodel/IXpsOMCoreProperties::SetCreator
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
 - IXpsOMCoreProperties.SetCreator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCoreProperties::SetCreator


## -description


Sets the <b>creator</b> property.


## -parameters




### -param creator [in]

The string to be written to the <b>creator</b> property. A <b>NULL</b> pointer clears the <b>creator</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>creator</b> property describes  the entity that is primarily responsible for making the content of
the resource.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

