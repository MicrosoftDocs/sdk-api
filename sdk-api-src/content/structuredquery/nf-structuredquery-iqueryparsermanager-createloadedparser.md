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

# IQueryParserManager::CreateLoadedParser


## -description


Creates a new instance of a <a href="https://msdn.microsoft.com/f022464d-9db6-42c8-a3fb-12c31ec48756">IQueryParser</a> interface implementation. This instance of the query parser is loaded with the schema for the specified catalog and is localized to a specified language. All other settings are initialized to default settings.


## -parameters




### -param pszCatalog [in]

Type: <b>LPCWSTR</b>

The name of the catalog to use. Permitted values are <code>SystemIndex</code> and an empty string (for a trivial schema with no properties).



### -param langidForKeywords [in]

Type: <b>LANGID</b>

The <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">LANGID</a> used to select the localized language for keywords.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://msdn.microsoft.com/f022464d-9db6-42c8-a3fb-12c31ec48756">IQueryParser</a> interface implementation.


### -param ppQueryParser [out, retval]

Type: <b>void**</b>


          Receives a pointer to the newly created parser. The calling application must release it by calling its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If %LOCALAPPDATA% is not available, then this method fails. You should call <a href="https://msdn.microsoft.com/54cb5501-bb53-4be5-8b0b-a2ea754c778a">IQueryParserManager::SetOption</a> to point to a different folder like %ProgramData%.



