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

# WICMapGuidToShortName function


## -description


Obtains the short name associated with a given GUID.


## -parameters




### -param guid [in]

Type: <b>REFGUID</b>

The GUID to retrieve the short name for.


### -param cchName [in]

Type: <b>UINT</b>

The size of the <i>wzName</i> buffer.


### -param wzName [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the short name associated with the GUID.


### -param pcchActual [out]

Type: <b>UINT*</b>

The actual size needed to retrieve the entire short name associated with the GUID.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Windows Imaging Component (WIC) short name mappings can be found within the following registry key:
            <pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{FAE3D380-FEA4-4623-8C75-C6B61110B681}</b>
         <b>Namespace</b>
            <b>...</b></pre>




