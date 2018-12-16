---
UID: NF:tuner.ILocator.put_SymbolRate
title: ILocator::put_SymbolRate
author: windows-sdk-content
description: The put_SymbolRate method sets the QPSK symbol rate.
old-location: mstv\ilocator_put_symbolrate.htm
tech.root: mstv
ms.assetid: 1eb91e22-b9b1-47dc-a2e4-cc64eeaacaaa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDigitalLocatorput_SymbolRate, ILocator interface [Microsoft TV Technologies],put_SymbolRate method, ILocator.put_SymbolRate, ILocator::put_SymbolRate, mstv.ilocator_put_symbolrate, put_SymbolRate, put_SymbolRate method [Microsoft TV Technologies], put_SymbolRate method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_SymbolRate
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
 - ILocator.put_SymbolRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocator::put_SymbolRate


## -description



The <b>put_SymbolRate</b> method sets the QPSK symbol rate.




## -parameters




### -param Rate [in]

Specifies the QPSK symbol rate. The rate is expressed in symbols per second.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693584(v=VS.85).aspx">get_SymbolRate</a>
 

 

