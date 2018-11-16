---
UID: NF:tuner.ILocator.get_OuterFECRate
title: ILocator::get_OuterFECRate
author: windows-sdk-content
description: The get_OuterFECRate method gets the outer FEC rate.
old-location: mstv\ilocator_get_outerfecrate.htm
tech.root: mstv
ms.assetid: 550103a8-dcf9-4a52-817a-61a589de4299
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDigitalLocatorget_OuterFECRate, ILocator interface [Microsoft TV Technologies],get_OuterFECRate method, ILocator.get_OuterFECRate, ILocator::get_OuterFECRate, get_OuterFECRate, get_OuterFECRate method [Microsoft TV Technologies], get_OuterFECRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_outerfecrate, tuner/ILocator::get_OuterFECRate
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
 - ILocator.get_OuterFECRate
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
- ILocator.get_OuterFECRate
: 
---

# ILocator::get_OuterFECRate


## -description



The <b>get_OuterFECRate</b> method gets the outer FEC rate.




## -parameters




### -param FEC [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/161c963f-55b2-4a17-a537-47de3326df0e">BinaryConvolutionCodeRate</a> that receives the outer FEC rate.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693581(v=VS.85).aspx">get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693582(v=VS.85).aspx">get_OuterFEC</a>



<a href="https://msdn.microsoft.com/library/Dd693588(v=VS.85).aspx">put_OuterFECRate</a>
 

 

