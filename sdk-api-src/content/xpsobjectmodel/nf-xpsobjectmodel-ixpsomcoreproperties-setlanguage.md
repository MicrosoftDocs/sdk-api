---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.SetLanguage
title: IXpsOMCoreProperties::SetLanguage
author: windows-sdk-content
description: Sets the language property.
old-location: xps\ixpsomcoreproperties_setlanguage.htm
old-project: printdocs
ms.assetid: e17901e8-9adb-488e-9c8d-6fa1351520ac
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMCoreProperties interface [XPS Documents and Packaging],SetLanguage method, IXpsOMCoreProperties.SetLanguage, IXpsOMCoreProperties::SetLanguage, SetLanguage, SetLanguage method [XPS Documents and Packaging], SetLanguage method [XPS Documents and Packaging],IXpsOMCoreProperties interface, xps.ixpsomcoreproperties_setlanguage, xpsobjectmodel/IXpsOMCoreProperties::SetLanguage
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMCoreProperties.SetLanguage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCoreProperties::SetLanguage


## -description


Sets the <b>language</b> property.


## -parameters




### -param language [in]

The string that contains the language value to be written to the <b>language</b> property. A <b>NULL</b> pointer clears the <b>language</b> property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>language</b> property describes the language of the resource's intellectual content.

Internet Engineering Task Force (IETF) RFC 3066 describes the recommended encoding for this property.




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

