---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProviderQuery.IsSubcategoryQuery
title: IFunctionDiscoveryProviderQuery::IsSubcategoryQuery (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Determines whether a query is for function instances in a specific subcategory.
old-location: ncd\ifunctiondiscoveryproviderquery_issubcategoryquery.htm
tech.root: FunDisc
ms.assetid: fa262e62-2e34-4881-915d-995d66fa6841
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProviderQuery interface,IsSubcategoryQuery method, IFunctionDiscoveryProviderQuery.IsSubcategoryQuery, IFunctionDiscoveryProviderQuery::IsSubcategoryQuery, IsSubcategoryQuery, IsSubcategoryQuery method, IsSubcategoryQuery method,IFunctionDiscoveryProviderQuery interface, functiondiscoveryprovider/IFunctionDiscoveryProviderQuery::IsSubcategoryQuery, ncd.ifunctiondiscoveryproviderquery_issubcategoryquery
ms.topic: method
f1_keywords: 
 - "functiondiscoveryprovider/IFunctionDiscoveryProviderQuery.IsSubcategoryQuery"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionDiscoveryProviderQuery::IsSubcategoryQuery


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a query is for function instances in a specific subcategory.


## -parameters




### -param pisSubcategoryQuery [out]

If this parameter is <b>TRUE</b>, there is a subcategory constraint in the query constraints collection.


### -param ppszConstraintValue [out]

The value of the subcategory constraint.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the provider does not support subcategories, the provider should return an <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a> with 0 instances in response to the query.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderquery">IFunctionDiscoveryProviderQuery</a>
 

 

