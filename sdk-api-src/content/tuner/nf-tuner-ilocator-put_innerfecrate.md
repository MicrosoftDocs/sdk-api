---
UID: NF:tuner.ILocator.put_InnerFECRate
title: ILocator::put_InnerFECRate
author: windows-sdk-content
description: The put_InnerFECRate method sets the inner FEC rate.
old-location: mstv\ilocator_put_innerfecrate.htm
tech.root: MSTV
ms.assetid: 009d1ddf-73ae-432b-adf2-a5a0067345fa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDigitalLocatorput_InnerFECRate, ILocator interface [Microsoft TV Technologies],put_InnerFECRate method, ILocator.put_InnerFECRate, ILocator::put_InnerFECRate, mstv.ilocator_put_innerfecrate, put_InnerFECRate, put_InnerFECRate method [Microsoft TV Technologies], put_InnerFECRate method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_InnerFECRate
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
 - ILocator.put_InnerFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- ILocator.put_InnerFECRate
: 
---

# ILocator::put_InnerFECRate


## -description



The <b>put_InnerFECRate</b> method sets the inner FEC rate.




## -parameters




### -param FEC [in]

Specifies the inner FEC rate. This parameter is a value of type <a href="https://msdn.microsoft.com/161c963f-55b2-4a17-a537-47de3326df0e">BinaryConvolutionCodeRate</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693581(v=VS.85).aspx">get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693585(v=VS.85).aspx">put_InnerFEC</a>



<a href="https://msdn.microsoft.com/library/Dd693588(v=VS.85).aspx">put_OuterFECRate</a>
 

 

