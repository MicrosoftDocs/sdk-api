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

# ITokenCollection::GetToken


## -description


Retrieves the position, length, and any overriding string of an individual token.


## -parameters




### -param i [in]

Type: <b>ULONG</b>


          The zero-based index of the desired token within the collection.
        


### -param pBegin [out]

Type: <b>ULONG*</b>

Receives the zero-based starting position of the specified token, in characters. This parameter can be <b>NULL</b>.


### -param pLength [out]

Type: <b>ULONG*</b>


          Receives the number of characters spanned by the token. This parameter can be <b>NULL</b>.
        


### -param ppsz [out]

Type: <b>LPWSTR*</b>


          Receives the overriding text for this token if available, or <b>NULL</b> if there is none.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



