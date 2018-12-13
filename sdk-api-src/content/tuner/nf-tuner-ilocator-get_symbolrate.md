---
UID: NF:tuner.ILocator.get_SymbolRate
title: ILocator::get_SymbolRate
author: windows-sdk-content
description: The get_SymbolRate method gets the QPSK symbol rate.
old-location: mstv\ilocator_get_symbolrate.htm
tech.root: mstv
ms.assetid: 828967df-6ce1-4320-ae83-7bfaec79f8c7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDigitalLocatorget_SymbolRate, ILocator interface [Microsoft TV Technologies],get_SymbolRate method, ILocator.get_SymbolRate, ILocator::get_SymbolRate, get_SymbolRate, get_SymbolRate method [Microsoft TV Technologies], get_SymbolRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_symbolrate, tuner/ILocator::get_SymbolRate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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



<a href="https://msdn.microsoft.com/library/Dd693589(v=VS.85).aspx">put_SymbolRate</a>
 

 

