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

# IApplicationAssociationRegistration::QueryAppIsDefault


## -description


Determines whether an application owns the registered default association for a given application level and type. Not intended for use in Windows 8.


## -parameters




### -param pszQuery [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that contains the file name extension or protocol of the application, such as .mp3 or http.


### -param atQueryType [in]

Type: <b><a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">ASSOCIATIONTYPE</a></b>

One of the <a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">ASSOCIATIONTYPE</a> enumeration values that specifies the type of the application named in <i>pszQuery</i>, such as file name extension or MIME type.


### -param alQueryLevel [in]

Type: <b><a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a></b>

One of the <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a> enumeration values that specifies the level of association, such as per-user or machine. This is typically <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">AL_EFFECTIVE</a>.


### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the registered name of the application.


### -param pfDefault [out]

Type: <b>BOOL*</b>

 When this method returns, contains <b>TRUE</b> if the application is the default; or <b>FALSE</b> otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>



<a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a>
 

 

