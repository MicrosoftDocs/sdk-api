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

# IUrlAccessor2::GetDisplayUrl


## -description



            Gets the user-friendly path for the URL item.
        


## -parameters




### -param wszDocUrl [out]

Type: <b>WCHAR[]</b>

Receives the display URL as a null-terminated Unicode string.
                


### -param dwSize [in]

Type: <b>DWORD</b>


                Size in <b>TCHAR</b><b>s</b>
                of <i>wszDocUrl</i>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>


                Receives a pointer to the number of
                <b>TCHAR</b><b>s</b> written
                to <i>wszDocUrl</i>, not including the terminating <b>NULL</b>. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Protocol handlers can reveal hierarchical or non-hierarchical stores. If the data store is organized hierarchically, users can scope their searches to a specified container object like a directory or folder. 




