---
UID: NF:tuner.ILocator.get_InnerFEC
title: ILocator::get_InnerFEC (tuner.h)
author: windows-sdk-content
description: The get_InnerFEC method gets the type of inner FEC that is used.
old-location: mstv\ilocator_get_innerfec.htm
tech.root: mstv
ms.assetid: aaa81a62-7e19-4d71-8378-77d6318a4e84
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDigitalLocatorget_InnerFEC, ILocator interface [Microsoft TV Technologies],get_InnerFEC method, ILocator.get_InnerFEC, ILocator::get_InnerFEC, get_InnerFEC, get_InnerFEC method [Microsoft TV Technologies], get_InnerFEC method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_innerfec, tuner/ILocator::get_InnerFEC
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
 - ILocator.get_InnerFEC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocator::get_InnerFEC


## -description



The <b>get_InnerFEC</b> method gets the type of inner FEC that is used.




## -parameters




### -param FEC [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/6910c51d-4176-49a3-be6b-6b072ad03fc1">FECMethod</a> that receives the type of inner FEC.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693581(v=VS.85).aspx">get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693582(v=VS.85).aspx">get_OuterFEC</a>



<a href="https://msdn.microsoft.com/library/Dd693585(v=VS.85).aspx">put_InnerFEC</a>
 

 

