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



