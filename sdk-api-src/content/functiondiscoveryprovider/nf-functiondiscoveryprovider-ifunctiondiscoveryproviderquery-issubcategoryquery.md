---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery.IsSubcategoryQuery
title: IFunctionDiscoveryProviderQuery::IsSubcategoryQuery
author: windows-sdk-content
description: Determines whether a query is for function instances in a specific subcategory.
old-location: ncd\ifunctiondiscoveryproviderquery_issubcategoryquery.htm
tech.root: FunDisc
ms.assetid: fa262e62-2e34-4881-915d-995d66fa6841
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFunctionDiscoveryProviderQuery interface,IsSubcategoryQuery method, IFunctionDiscoveryProviderQuery.IsSubcategoryQuery, IFunctionDiscoveryProviderQuery::IsSubcategoryQuery, IsSubcategoryQuery, IsSubcategoryQuery method, IsSubcategoryQuery method,IFunctionDiscoveryProviderQuery interface, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::IsSubcategoryQuery, ncd.ifunctiondiscoveryproviderquery_issubcategoryquery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProviderQuery.IsSubcategoryQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProviderQuery::IsSubcategoryQuery


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a query is for function instances in a specific subcategory.


## -parameters




### -param pisSubcategoryQuery

TBD


### -param ppszConstraintValue [out]

The value of the subcategory constraint.


#### - pisInstanceQuery [out]

If this parameter is <b>TRUE</b>, there is a subcategory constraint in the query constraints collection.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the provider does not support subcategories, the provider should return an <a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a> with 0 instances in response to the query.




## -see-also




<a href="https://msdn.microsoft.com/97468045-faa5-4690-8db5-50ee9656517b">IFunctionDiscoveryProviderQuery</a>
 

 

