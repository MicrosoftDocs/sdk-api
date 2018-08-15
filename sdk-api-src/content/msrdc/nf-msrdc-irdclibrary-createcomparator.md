---
UID: NF:msrdc.IRdcLibrary.CreateComparator
title: IRdcLibrary::CreateComparator
author: windows-sdk-content
description: Creates a signature comparator.
old-location: rdc\irdclibrary_createcomparator.htm
old-project: Rdc
ms.assetid: 21e83ed0-974a-470f-8a7f-1776f1575100
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CreateComparator, CreateComparator method [Remote Differential Compression], CreateComparator method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],CreateComparator method, IRdcLibrary.CreateComparator, IRdcLibrary::CreateComparator, MSRDC_DEFAULT_COMPAREBUFFER, MSRDC_MAXIMUM_COMPAREBUFFER, MSRDC_MINIMUM_COMPAREBUFFER, fs.irdclibrary_createcomparator, msrdc/IRdcLibrary::CreateComparator, rdc.irdclibrary_createcomparator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsRdc.dll
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcLibrary.CreateComparator
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

