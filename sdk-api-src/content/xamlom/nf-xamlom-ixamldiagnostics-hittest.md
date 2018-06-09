---
UID: NF:xamlom.IXamlDiagnostics.HitTest
title: IXamlDiagnostics::HitTest
author: windows-sdk-content
description: Gets all elements in the visual tree that fall within the specified rectangle.
old-location: xaml_diagnostics\ixamldiagnostics_hittest.htm
old-project: xaml_diagnostics
ms.assetid: B7722F49-F477-4D24-9183-BC09A4A12730
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: HitTest, HitTest method, HitTest method,IXamlDiagnostics interface, IXamlDiagnostics interface,HitTest method, IXamlDiagnostics.HitTest, IXamlDiagnostics::HitTest, xaml_diagnostics.ixamldiagnostics_hittest, xamlom/IXamlDiagnostics::HitTest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VisualMutationType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IXamlDiagnostics.HitTest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXamlDiagnostics::HitTest


## -description


Gets all elements in the visual tree that fall within the specified rectangle.


## -parameters




### -param rect [in]

The area to hit test.


### -param pCount [out]

The size of the array.


### -param ppInstanceHandles [out]

An array containing all elements.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method performs a hit test on the XAML visual tree and will return all elements
    regardless if they are enabled or invisible for hit testing. This method does not return collapsed elements as they do not participate in layout. <a href="https://msdn.microsoft.com/83971154-4E40-474C-91AD-2436B1D02CB8">AdviseVisualTreeChange</a>
    must be called before this method. The element does not need to be fully enclosed in the 
    <i>rect</i> area to be returned.




## -see-also




<a href="https://msdn.microsoft.com/1BCE3EC3-8B48-4F16-8E91-78776C07F309">IXamlDiagnostics</a>
 

 

