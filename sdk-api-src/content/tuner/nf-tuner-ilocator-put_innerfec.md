---
UID: NF:tuner.ILocator.put_InnerFEC
title: ILocator::put_InnerFEC
author: windows-sdk-content
description: The put_InnerFEC method sets the type of inner FEC to use.
old-location: mstv\ilocator_put_innerfec.htm
old-project: mstv
ms.assetid: 3ba6cfdf-2095-489c-a899-4b4305758ccb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDigitalLocatorput_InnerFEC, ILocator interface [Microsoft TV Technologies],put_InnerFEC method, ILocator.put_InnerFEC, ILocator::put_InnerFEC, mstv.ilocator_put_innerfec, put_InnerFEC, put_InnerFEC method [Microsoft TV Technologies], put_InnerFEC method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_InnerFEC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ILocator.put_InnerFEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILocator::put_InnerFEC


## -description



The <b>put_InnerFEC</b> method sets the type of inner FEC to use.




## -parameters




### -param FEC [in]

Specifies the inner FEC. This parameter is a value of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff559594">FECMethod</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="mstv.idigitallocator_get_innerfec">get_InnerFEC</a>



<a href="mstv.idigitallocator_put_innerfecrate">put_InnerFECRate</a>



<a href="mstv.idigitallocator_put_outerfec">put_OuterFEC</a>
 

 

