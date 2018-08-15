---
UID: NF:xamlom.IVisualTreeService.AddChild
title: IVisualTreeService::AddChild
author: windows-sdk-content
description: Adds a child element to the collection at the specified index.
old-location: xaml_diagnostics\ivisualtreeservice_addchild.htm
old-project: xaml_diagnostics
ms.assetid: 0F3BFACA-0B4C-4CC5-A48B-BD3921728612
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddChild, AddChild method, AddChild method,IVisualTreeService interface, IVisualTreeService interface,AddChild method, IVisualTreeService.AddChild, IVisualTreeService::AddChild, xaml_diagnostics.ivisualtreeservice_addchild, xamlom/IVisualTreeService::AddChild
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
 - IVisualTreeService.AddChild
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IVisualTreeService::AddChild


## -description


Adds a child element to the collection at the specified index.


## -parameters




### -param parent [in]

A handle to the collection object.


### -param child [in]

A handle to the element to place into the collection. This can be newly created through <a href="https://msdn.microsoft.com/214BE795-5883-4761-9040-2C7A679F5258">CreateInstance</a> or shared, such as <b>SolidColorBrush</b>.


### -param index [in]

Location in <i>parent</i> collection at which to insert <i>child</i> element.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="https://msdn.microsoft.com/951A4C1F-B176-4D18-821A-CEAD1116B8BE">MetadataBit::IsValueCollection</a>set.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

