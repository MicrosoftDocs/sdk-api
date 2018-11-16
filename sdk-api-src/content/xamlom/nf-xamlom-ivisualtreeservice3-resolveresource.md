---
UID: NF:xamlom.IVisualTreeService3.ResolveResource
title: IVisualTreeService3::ResolveResource
author: windows-sdk-content
description: Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index.
old-location: xaml_diagnostics\ivisualtreeservice3_resolveresource.htm
tech.root: xaml_diagnostics
ms.assetid: 7DDF1FD0-AD9B-4679-831D-CEDF6524181B
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVisualTreeService3 interface,ResolveResource method, IVisualTreeService3.ResolveResource, IVisualTreeService3::ResolveResource, ResolveResource, ResolveResource method, ResolveResource method,IVisualTreeService3 interface, xaml_diagnostics.ivisualtreeservice3_resolveresource, xamlom/IVisualTreeService3::ResolveResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
 - IVisualTreeService3.ResolveResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xamlom.h
: 
- IVisualTreeService3.ResolveResource
: 
---

# IVisualTreeService3::ResolveResource


## -description


Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index.


## -parameters




### -param resourceContext [in]

The context of the resource.


### -param resourceName [in]

The name of the resource.


### -param resourceType [in]

The type of the resource.


### -param propertyIndex [in]

The index of the property to apply the resource to.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If no resource was found, or the resource type was invalid, <a href="https://msdn.microsoft.com/F1C11F32-9524-49D6-89DD-C89E4A81720A">IVisualTreeServiceCallback2</a>  will be notified.

Call <a href="https://msdn.microsoft.com/E836FE12-A49A-427C-8013-F1AFBD2C08A2">GetDictionaryItem</a> to get a <i>resourceContext</i> and give better resolution context for <b>ResolveResource</b>.




## -see-also




<a href="https://msdn.microsoft.com/20AD2DC4-388E-458E-AA44-8B2F3464FD6C">IVisualTreeService3</a>
 

 

