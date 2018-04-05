---
UID: NF:xamlom.IVisualTreeService.ClearProperty
title: IVisualTreeService::ClearProperty method
author: windows-driver-content
description: Clears the specified property on a XAML element.
old-location: xaml_diagnostics\ivisualtreeservice_clearproperty.htm
old-project: xaml_diagnostics
ms.assetid: BB875AD0-271D-4913-9811-5A5102B3E331
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: ClearProperty method, ClearProperty method, IVisualTreeService interface, ClearProperty,IVisualTreeService.ClearProperty, IVisualTreeService, IVisualTreeService interface, ClearProperty method, IVisualTreeService::ClearProperty, xaml_diagnostics.ivisualtreeservice_clearproperty, xamlom/IVisualTreeService::ClearProperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VisualMutationType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xamlom.h
api_name:
-	IVisualTreeService.ClearProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeService::ClearProperty method


## -description


Clears the specified property on a XAML element.


## -parameters




### -param instanceHandle [in]

A handle to the element to set the property on.


### -param propertyIndex [in]

The index (in the XAML runtime cache) of the property to clear.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

