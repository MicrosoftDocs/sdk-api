---
UID: NF:tuner.ILocator.get_OuterFEC
title: ILocator::get_OuterFEC
author: windows-sdk-content
description: The get_OuterFEC method gets the type of outer FEC that is used.
old-location: mstv\ilocator_get_outerfec.htm
tech.root: MSTV
ms.assetid: d32937e1-0b8c-485e-8bd0-df15ab2ed373
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDigitalLocatorget_OuterFEC, ILocator interface [Microsoft TV Technologies],get_OuterFEC method, ILocator.get_OuterFEC, ILocator::get_OuterFEC, get_OuterFEC, get_OuterFEC method [Microsoft TV Technologies], get_OuterFEC method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_outerfec, tuner/ILocator::get_OuterFEC
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
 - ILocator.get_OuterFEC
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
- ILocator.get_OuterFEC
: 
---

# ILocator::get_OuterFEC


## -description



The <b>get_OuterFEC</b> method gets the type of outer FEC that is used.




## -parameters




### -param FEC [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/6910c51d-4176-49a3-be6b-6b072ad03fc1">FECMethod</a> that receives the type of outer FEC.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693580(v=VS.85).aspx">get_InnerFEC</a>



<a href="https://msdn.microsoft.com/library/Dd693583(v=VS.85).aspx">get_OuterFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693587(v=VS.85).aspx">put_OuterFEC</a>
 

 

