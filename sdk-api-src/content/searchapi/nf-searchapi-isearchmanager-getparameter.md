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

# ISearchManager::GetParameter


## -description


Not supported.

This method returns E_INVALIDARG when called.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>


                    There are currently no valid parameters in this version of search (WDS 3.0).


### -param ppValue [out, retval]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>**</b>


                    Returns a value in an undefined state as there are no properties currently defined to retrieve values from.


## -returns



Type: <b>HRESULT</b>

This method returns E_InvalidArg as an error code when called.




## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



