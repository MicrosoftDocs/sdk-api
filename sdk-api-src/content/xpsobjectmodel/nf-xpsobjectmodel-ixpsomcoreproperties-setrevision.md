---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetRevision
title: IXpsOMCoreProperties::SetRevision
author: windows-sdk-content
description: Sets the revision property.
old-location: xps\ixpsomcoreproperties_setrevision.htm
old-project: printdocs
ms.assetid: 7e2ef3b4-64dd-402e-a282-0ed01e588337
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetRevision method, IXpsOMCoreProperties.SetRevision, IXpsOMCoreProperties::SetRevision, SetRevision, SetRevision method [XPS Documents and Packaging], SetRevision method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setrevision, xpsobjectmodel/IXpsOMCoreProperties::SetRevision
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
 - IXpsOMCoreProperties.SetRevision
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

