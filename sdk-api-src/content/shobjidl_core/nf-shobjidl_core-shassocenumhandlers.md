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

# SHAssocEnumHandlers function


## -description


Returns an enumeration object for a specified set of file name extension handlers.


## -parameters




### -param pszExtra [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated buffer that contains a single file type extension, for instance ".jpg". Only handlers associated with the given extension are enumerated. If this value is <b>NULL</b>, all handlers for all extensions are enumerated.


### -param afFilter [in]

Type: <b>ASSOC_FILTER</b>

Specifies the enumeration handler filter applied to the full list of handlers that results from the value given in <i>pszExtra</i>. One of the following values.



#### ASSOC_FILTER_NONE

Return all handlers.



#### ASSOC_FILTER_RECOMMENDED

Return only recommended handlers. A handler sets its recommended status in the registry when it is installed. An initial status of non-recommended can later be promoted to recommended as a result of user action.


### -param ppEnumHandler [out]

Type: <b><a href="https://msdn.microsoft.com/c8b11157-4d00-4ab1-aea5-ce8ae35c43ce">IEnumAssocHandlers</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/c8b11157-4d00-4ab1-aea5-ce8ae35c43ce">IEnumAssocHandlers</a> object.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



