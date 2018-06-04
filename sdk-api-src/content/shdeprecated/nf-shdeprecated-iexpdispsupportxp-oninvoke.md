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

# IExpDispSupportXP::OnInvoke


## -description


Not implemented.


## -parameters




### -param dispidMember

Type: <b>DISPID</b>

Specifies a dispatch ID that identifies the member being invoked.


### -param iid

Type: <b>REFIID</b>

Reserved. Must be IID_NULL.


### -param lcid

Type: <b>LCID</b>

Specifies a locale ID providing a locale context in which to interpret arguments. Applications that do not support multiple national languages can ignore this parameter.


### -param wFlags

Type: <b>WORD</b>

Specifies flags describing the context of the call.


### -param pdispparams [in]

Type: <b><a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a>*</b>

Specifies a pointer to a <a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a> structure containing an array of arguments, an array of argument DISPIDs for named arguments, and counts for the number of elements in the arrays.


### -param pVarResult [out]

Type: <b>VARIANT*</b>

Receives a pointer to the location where the result is to be stored, or <b>NULL</b> if the calling application expects no result. This argument is ignored if DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF is specified.


### -param pexcepinfo [out]

Type: <b>EXCEPINFO*</b>

Receives a pointer to a structure that contains exception information. This structure should be filled in if DISP_E_EXCEPTION is returned. Can be <b>NULL</b>.


### -param puArgErr [out]

Type: <b>UINT*</b>

Receives the index within the <b>rgvarg</b> member of the <a href="a16e5a21-766e-4287-b039-13429aa78f8b">DISPPARAMS</a> structure of the first argument that has an error.


## -returns



Type: <b>HRESULT</b>

Returns E_NOTIMPL.



