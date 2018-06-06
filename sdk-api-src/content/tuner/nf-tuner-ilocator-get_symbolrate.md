---
UID: NF:tuner.ILocator.get_SymbolRate
title: ILocator::get_SymbolRate
author: windows-sdk-content
description: The get_SymbolRate method gets the QPSK symbol rate.
old-location: mstv\ilocator_get_symbolrate.htm
old-project: mstv
ms.assetid: 828967df-6ce1-4320-ae83-7bfaec79f8c7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDigitalLocatorget_SymbolRate, ILocator interface [Microsoft TV Technologies],get_SymbolRate method, ILocator.get_SymbolRate, ILocator::get_SymbolRate, get_SymbolRate, get_SymbolRate method [Microsoft TV Technologies], get_SymbolRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_symbolrate, tuner/ILocator::get_SymbolRate
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
 - ILocator.get_SymbolRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILocator::get_SymbolRate


## -description



The <b>get_SymbolRate</b> method gets the QPSK symbol rate.




## -parameters




### -param Rate [out]

Receives the QPSK symbol rate. The rate is expressed in symbols per second.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="mstv.idigitallocator_put_symbolrate">put_SymbolRate</a>
 

 

