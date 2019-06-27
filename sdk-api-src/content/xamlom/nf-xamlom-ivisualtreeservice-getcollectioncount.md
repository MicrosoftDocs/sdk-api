---
UID: NF:xamlom.IVisualTreeService.GetCollectionCount
title: IVisualTreeService::GetCollectionCount (xamlom.h)
author: windows-sdk-content
description: Gets the count of a collection.
old-location: xaml_diagnostics\ivisualtreeservice_getcollectioncount.htm
tech.root: xaml_diagnostics
ms.assetid: BB6D0885-27BD-4DF6-A48A-570345F1EE14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCollectionCount, GetCollectionCount method, GetCollectionCount method,IVisualTreeService interface, IVisualTreeService interface,GetCollectionCount method, IVisualTreeService.GetCollectionCount, IVisualTreeService::GetCollectionCount, xaml_diagnostics.ivisualtreeservice_getcollectioncount, xamlom/IVisualTreeService::GetCollectionCount
ms.topic: method
f1_keywords: 
 - "xamlom/IVisualTreeService.GetCollectionCount"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
    and should only call this method if the property has <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit::IsValueCollection</a>set.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>
 

 

