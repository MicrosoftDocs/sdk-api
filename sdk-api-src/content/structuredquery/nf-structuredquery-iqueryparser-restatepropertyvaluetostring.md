---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IQueryParser::RestatePropertyValueToString


## -description


Restates a specified property for a condition as a query string. 


## -parameters




### -param pCondition [in]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>*</b>

A condition to be restated as a query string.


### -param fUseEnglish [in]

Type: <b>BOOL</b>

Reserved. Must be <b>FALSE</b>.


### -param ppszPropertyName [out]

Type: <b>LPWSTR*</b>

Receives a pointer to the property name as a Unicode string. The calling application must free the string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.


### -param ppszQueryString [out]

Type: <b>LPWSTR*</b>


                  Receives a pointer to a query string for that property. The calling application must free the string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the leaf nodes of the condition contain more than one property name, or no property name at all, E_INVALIDARG is returned.
                



