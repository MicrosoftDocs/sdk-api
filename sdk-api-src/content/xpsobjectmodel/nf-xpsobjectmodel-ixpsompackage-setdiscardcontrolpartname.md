---
UID: NF:xpsobjectmodel.IXpsOMPackage.SetDiscardControlPartName
title: IXpsOMPackage::SetDiscardControlPartName
author: windows-sdk-content
description: Sets the name of the discard control part in the XPS package.
old-location: xps\ixpsompackage_setdiscardcontrolpartname.htm
tech.root: printdocs
ms.assetid: ce45f7cf-33ed-4e15-9f65-549ab2c8c8be
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IXpsOMPackage interface [XPS Documents and Packaging],SetDiscardControlPartName method, IXpsOMPackage.SetDiscardControlPartName, IXpsOMPackage::SetDiscardControlPartName, SetDiscardControlPartName, SetDiscardControlPartName method [XPS Documents and Packaging], SetDiscardControlPartName method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_setdiscardcontrolpartname, xpsobjectmodel/IXpsOMPackage::SetDiscardControlPartName
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
 - IXpsOMPackage.SetDiscardControlPartName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackage::SetDiscardControlPartName


## -description


Sets the name of the discard control part in the XPS package.


## -parameters




### -param discardControlPartUri [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the name of the discard control part to be assigned to the XPS package. A <b>NULL</b> pointer releases any previously assigned discard control part.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

