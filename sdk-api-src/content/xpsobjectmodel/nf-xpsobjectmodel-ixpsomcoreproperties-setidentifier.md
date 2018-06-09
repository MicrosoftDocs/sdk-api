---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetIdentifier
title: IXpsOMCoreProperties::SetIdentifier
author: windows-sdk-content
description: Sets the identifier property.
old-location: xps\ixpsomcoreproperties_setidentifier.htm
old-project: printdocs
ms.assetid: 8ad5a359-77f6-4b11-9c1c-2e4094be65d0
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetIdentifier method, IXpsOMCoreProperties.SetIdentifier, IXpsOMCoreProperties::SetIdentifier, SetIdentifier, SetIdentifier method [XPS Documents and Packaging], SetIdentifier method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setidentifier, xpsobjectmodel/IXpsOMCoreProperties::SetIdentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
 - IXpsOMCoreProperties.SetIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCoreProperties::SetIdentifier


## -description


Sets the <b>identifier</b> property.


## -parameters




### -param identifier [in]

The string to be written to the <b>identifier</b> property. A <b>NULL</b> pointer clears the <b>identifier</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>identifier</b> property is an unambiguous reference to the resource within a user-defined or application-specific
context.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

