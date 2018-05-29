---
UID: NF:structuredquery.ISchemaLocalizerSupport.Localize
title: ISchemaLocalizerSupport::Localize
author: windows-sdk-content
description: Localizes keywords from an input string.
old-location: search\_search_ISchemaLocalizerSupport_Localize.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemalocalizersupport\localize.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ISchemaLocalizerSupport interface [search],Localize method, ISchemaLocalizerSupport.Localize, ISchemaLocalizerSupport::Localize, Localize, Localize method [search], Localize method [search],ISchemaLocalizerSupport interface, _search_ISchemaLocalizerSupport_Localize, search._search_ISchemaLocalizerSupport_Localize, structuredquery/ISchemaLocalizerSupport::Localize
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
-	ISchemaLocalizerSupport.Localize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISchemaLocalizerSupport::Localize


## -description


Localizes keywords from an input string.


## -parameters




### -param pszGlobalString [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string to be localized. It may be in one of two forms: (1) a set of keywords separated by the vertical bar character (Unicode character code 007C) (for example "date modified|modified|modification date"), or (2) a string of the form "@some.dll,-12345". This example refers to resource ID 12345 of the some.dll binary. That resource must be a string of the previous (1) form.


### -param ppszLocalString [out, retval]

Type: <b>LPWSTR*</b>

Returns a null-terminated Unicode string that is the localized string. The calling application must free the returned string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>. If the method does not succeed, this parameter is set to <b>NULL</b>.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or S_FALSE otherwise.



