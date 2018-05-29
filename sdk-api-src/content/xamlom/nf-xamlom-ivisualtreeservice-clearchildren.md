---
UID: NF:xamlom.IVisualTreeService.ClearChildren
title: IVisualTreeService::ClearChildren
author: windows-sdk-content
description: Clears all child elements from the parent collection.
old-location: xaml_diagnostics\ivisualtreeservice_clearchildren.htm
old-project: xaml_diagnostics
ms.assetid: E32B07F5-BB62-435A-A869-36A0E93915D9
ms.author: windowssdkdev
ms.date: 03/19/2018
ms.keywords: ClearChildren, ClearChildren method, ClearChildren method,IVisualTreeService interface, IVisualTreeService interface,ClearChildren method, IVisualTreeService.ClearChildren, IVisualTreeService::ClearChildren, xaml_diagnostics.ivisualtreeservice_clearchildren, xamlom/IVisualTreeService::ClearChildren
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
req.typenames: VisualMutationType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xamlom.h
api_name:
-	IVisualTreeService.ClearChildren
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeService::ClearChildren


## -description


Clears all child elements from the parent collection.


## -parameters




### -param parent [in]

A handle to the collection object.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="https://msdn.microsoft.com/951A4C1F-B176-4D18-821A-CEAD1116B8BE">MetadataBit::IsValueCollection</a>
    set.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

