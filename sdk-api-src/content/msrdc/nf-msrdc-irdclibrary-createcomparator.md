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

# IRdcLibrary::CreateComparator


## -description


The <b>CreateComparator</b> method 
    creates a signature comparator.


## -parameters




### -param iSeedSignaturesFile [in]

An <a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a> interface pointer initialized to 
      read the seed signatures.


### -param comparatorBufferSize [in]

Specifies the size of the comparator buffer. The range is from 
      <b>MSRDC_MINIMUM_COMPAREBUFFER</b> to 
      <b>MSRDC_MAXIMUM_COMPAREBUFFER</b>.



#### MSRDC_MINIMUM_COMPAREBUFFER (100000)

Minimum size of a comparator buffer.



#### MSRDC_DEFAULT_COMPAREBUFFER (3200000)

Default size of a comparator buffer. Used if zero (0) is passed for 
        <i>comparatorBufferSize</i>.



#### MSRDC_MAXIMUM_COMPAREBUFFER (1073741824)

Maximum size of a comparator buffer. (1&lt;&lt;30)


### -param iComparator [out]

Pointer to a location that will receive an 
      <a href="https://msdn.microsoft.com/ad39b922-3271-491e-b74b-80a1f647e663">IRdcComparator</a> interface pointer. On a successful return 
      the interface will be initialized on return. Callers must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller must create a separate signature comparator for each 
    level of recursion.




## -see-also




<a href="https://msdn.microsoft.com/ad39b922-3271-491e-b74b-80a1f647e663">IRdcComparator</a>



<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>
 

 

