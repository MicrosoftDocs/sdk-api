---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetLastModifiedBy
title: IXpsOMCoreProperties::SetLastModifiedBy
author: windows-sdk-content
description: Sets the lastModifiedBy property.
old-location: xps\ixpsomcoreproperties_setlastmodifiedby.htm
tech.root: printdocs
ms.assetid: 4c19e7c8-d790-42b8-a0c4-bfd95c7de2c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetLastModifiedBy method, IXpsOMCoreProperties.SetLastModifiedBy, IXpsOMCoreProperties::SetLastModifiedBy, SetLastModifiedBy, SetLastModifiedBy method [XPS Documents and Packaging], SetLastModifiedBy method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setlastmodifiedby, xpsobjectmodel/IXpsOMCoreProperties::SetLastModifiedBy
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
 - IXpsOMCoreProperties.SetLastModifiedBy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCoreProperties::SetLastModifiedBy


## -description


Sets the <b>lastModifiedBy</b> property.


## -parameters




### -param lastModifiedBy [in]

The string that contains the value to be written to the <b>lastModifiedBy</b> property. A <b>NULL</b> pointer clears the <b>lastModifiedBy</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>lastModifiedBy</b> property describes the user who performs the last modification.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

