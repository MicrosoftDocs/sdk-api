---
UID: NF:xamlom.IVisualTreeService.GetEnums
title: IVisualTreeService::GetEnums
author: windows-sdk-content
description: Gets an array of all the enums defined in the XAML runtime and the total count.
old-location: xaml_diagnostics\ivisualtreeservice_getenums.htm
old-project: xaml_diagnostics
ms.assetid: 95D6F754-C1D0-4B8E-8E31-999CAE0EDF02
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetEnums, GetEnums method, GetEnums method,IVisualTreeService interface, IVisualTreeService interface,GetEnums method, IVisualTreeService.GetEnums, IVisualTreeService::GetEnums, xaml_diagnostics.ivisualtreeservice_getenums, xamlom/IVisualTreeService::GetEnums
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xamlom.h
req.include-header: 
req.redist: 
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
 - IVisualTreeService.GetEnums
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeService::GetEnums


## -description


Gets an array of all the enums defined in the XAML runtime and the total
    count.


## -parameters




### -param pCount [out]

The count of enums in the array.


### -param ppEnums [out]

An array of enums defined in the XAML runtime.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. This method should not fail in normal conditions.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

