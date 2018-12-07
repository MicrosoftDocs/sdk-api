---
UID: NF:xamlom.IVisualTreeService.RemoveChild
title: IVisualTreeService::RemoveChild
author: windows-sdk-content
description: Removes the child element from the specified index.
old-location: xaml_diagnostics\ivisualtreeservice_removechild.htm
tech.root: xaml_diagnostics
ms.assetid: 6D53C961-7E85-4275-8D65-454684606290
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVisualTreeService interface,RemoveChild method, IVisualTreeService.RemoveChild, IVisualTreeService::RemoveChild, RemoveChild, RemoveChild method, RemoveChild method,IVisualTreeService interface, xaml_diagnostics.ivisualtreeservice_removechild, xamlom/IVisualTreeService::RemoveChild
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
 - IVisualTreeService.RemoveChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVisualTreeService::RemoveChild


## -description


Removes the child element from the specified index.


## -parameters




### -param parent [in]

A handle to the collection object.


### -param index [in]

Location in <i>parent</i> collection at which to remove the child element.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. The method will fail if index is outside
    of the collection range.




## -remarks



For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="https://msdn.microsoft.com/951A4C1F-B176-4D18-821A-CEAD1116B8BE">MetadataBit::IsValueCollection</a>set.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

