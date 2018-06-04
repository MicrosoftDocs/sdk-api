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

# MFGetMFTMerit function


## -description


Gets the merit value of a hardware codec.


## -parameters




### -param pMFT [in, out]

A pointer to the <b>IUnknown</b> interface of the Media Foundation transform (MFT) that represents the codec.


### -param cbVerifier [in]

The size, in bytes, of the <i>verifier</i> array.


### -param verifier [in]

The address of a buffer that contains one of the following:

<ul>
<li>The class identifier (CLSID) of the MFT.</li>
<li>A null-terminated wide-character string that contains the symbol link for the underlying hardware device. Include the size of the terminating null in the value of <i>cbVerifier</i>.</li>
</ul>

### -param merit [out]

Receives the merit value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The function fails if the MFT does not represent a hardware device with a valid Output Protection Manager (OPM) certificate.
      




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/51987a79-78bf-41b2-8349-8c2725dd89d6">OPM_GET_CODEC_INFO</a>
 

 

