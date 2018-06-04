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

# PFN_CRYPT_XML_DATA_PROVIDER_READ callback function


## -description


The <i>PFN_CRYPT_XML_DATA_PROVIDER_READ</i> callback function reads XML data.


## -parameters




### -param *pvCallbackState [in, out]

A pointer to an application defined argument that is passed to the calling function.


### -param *pbData [out]

A pointer to the buffer that receives the data to be read.


### -param cbData [in]

The size, in bytes, of the data to be read.


### -param *pcbRead [out]

A pointer to a variable that receives the number of bytes actually read.


## -returns



 The <i>PFN_CRYPT_XML_DATA_PROVIDER_READ</i> callback function returns a value when one of the 
    following conditions occurs:

<ul>
<li>A write operation completes on the data provider</li>
<li>The number of bytes requested is read</li>
<li>An error occurs</li>
</ul>
If the function succeeds, the function returns NO_ERROR.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

If the value of <i>pcbRead</i> equals zero, then there is no more data available.




## -remarks



 The callback function does not return a value unless the number of bytes specified in <i>cbData</i> 
 is available or  the last block of data has been read.



