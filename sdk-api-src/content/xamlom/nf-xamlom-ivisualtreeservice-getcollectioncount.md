---
UID: NF:xamlom.IVisualTreeService.GetCollectionCount
title: IVisualTreeService::GetCollectionCount
author: windows-sdk-content
description: Gets the count of a collection.
old-location: xaml_diagnostics\ivisualtreeservice_getcollectioncount.htm
old-project: xaml_diagnostics
ms.assetid: BB6D0885-27BD-4DF6-A48A-570345F1EE14
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCollectionCount, GetCollectionCount method, GetCollectionCount method,IVisualTreeService interface, IVisualTreeService interface,GetCollectionCount method, IVisualTreeService.GetCollectionCount, IVisualTreeService::GetCollectionCount, xaml_diagnostics.ivisualtreeservice_getcollectioncount, xamlom/IVisualTreeService::GetCollectionCount
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
 - IVisualTreeService.GetCollectionCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeService::GetCollectionCount


## -description


Gets the count of a collection.


## -parameters




### -param instanceHandle [in]

A handle to the collection object.


### -param pCollectionSize [out]

The number of elements in the collection.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="https://msdn.microsoft.com/951A4C1F-B176-4D18-821A-CEAD1116B8BE">MetadataBit::IsValueCollection</a>set.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

