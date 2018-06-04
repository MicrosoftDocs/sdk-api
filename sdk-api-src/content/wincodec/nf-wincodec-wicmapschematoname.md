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

# WICMapSchemaToName function


## -description


Obtains the name associated with a given schema.


## -parameters




### -param guidMetadataFormat [in]

Type: <b><a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">REFGUID</a></b>

The metadata format GUID.


### -param pwzSchema [in]

Type: <b>LPWSTR</b>

The URI string of the schema for which the name is to be retrieved.


### -param cchName [in]

Type: <b>UINT</b>

The size of the <i>wzName</i> buffer.


### -param wzName [in, out]

Type: <b>WCHAR*</b>

A pointer to a buffer that receives the schema's name.

To obtain the required buffer size, call <b>WICMapSchemaToName</b> with <i>cchName</i> set to 0 and <i>wzName</i> set to <b>NULL</b>.


### -param pcchActual [out]

Type: <b>UINT</b>

The actual buffer size needed to retrieve the entire schema name.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can extend the schema name mapping by adding to the following registry key:


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{FAE3D380-FEA4-4623-8C75-C6B61110B681}</b>
         <b>Schemas</b>
            <b>BB5ACC38-F216-4CEC-A6C5-5F6E739763A9</b>
               <b>...</b></pre>


For more information, see <a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled Codec</a>.



