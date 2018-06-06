---
UID: NF:xpsobjectmodel.IXpsOMPath.SetAccessibilityShortDescription
title: IXpsOMPath::SetAccessibilityShortDescription
author: windows-sdk-content
description: Sets the short textual description of the object's contents.
old-location: xps\ixpsompath_setaccessibilityshortdescription.htm
old-project: printdocs
ms.assetid: 1e078817-be7c-493c-9b46-9c9f4068745c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetAccessibilityShortDescription method, IXpsOMPath.SetAccessibilityShortDescription, IXpsOMPath::SetAccessibilityShortDescription, SetAccessibilityShortDescription, SetAccessibilityShortDescription method [XPS Documents and Packaging], SetAccessibilityShortDescription method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setaccessibilityshortdescription, xpsobjectmodel/IXpsOMPath::SetAccessibilityShortDescription
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
 - IXpsOMPath.SetAccessibilityShortDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::SetAccessibilityShortDescription


## -description


Sets the short textual description of the object's contents. This description is used by accessibility clients to describe the object.


## -parameters




### -param shortDescription [in]

The  short textual description of the object's contents.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



In the document markup, the value that is set in <i>shortDescription</i> will be that of  the <b>AutomationProperties.Name</b> attribute of the  <b>Path</b> element.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

