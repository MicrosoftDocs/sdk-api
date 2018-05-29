---
UID: NF:structuredquery.IQueryParser.RestatePropertyValueToString
title: IQueryParser::RestatePropertyValueToString
author: windows-sdk-content
description: Restates a specified property for a condition as a query string.
old-location: search\_search_IQueryParser_RestatePropertyValueToString.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\restatepropertyvaluetostring.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IQueryParser interface [search],RestatePropertyValueToString method, IQueryParser.RestatePropertyValueToString, IQueryParser::RestatePropertyValueToString, RestatePropertyValueToString, RestatePropertyValueToString method [search], RestatePropertyValueToString method [search],IQueryParser interface, _search_IQueryParser_RestatePropertyValueToString, search._search_IQueryParser_RestatePropertyValueToString, structuredquery/IQueryParser::RestatePropertyValueToString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IQueryParser.RestatePropertyValueToString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
                



