---
UID: NF:tuner.ILocator.put_InnerFEC
title: ILocator::put_InnerFEC
author: windows-sdk-content
description: The put_InnerFEC method sets the type of inner FEC to use.
old-location: mstv\ilocator_put_innerfec.htm
tech.root: mstv
ms.assetid: 3ba6cfdf-2095-489c-a899-4b4305758ccb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDigitalLocatorput_InnerFEC, ILocator interface [Microsoft TV Technologies],put_InnerFEC method, ILocator.put_InnerFEC, ILocator::put_InnerFEC, mstv.ilocator_put_innerfec, put_InnerFEC, put_InnerFEC method [Microsoft TV Technologies], put_InnerFEC method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_InnerFEC
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
 - ILocator.put_InnerFEC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocator::put_InnerFEC


## -description



The <b>put_InnerFEC</b> method sets the type of inner FEC to use.




## -parameters




### -param FEC [in]

Specifies the inner FEC. This parameter is a value of type <a href="https://msdn.microsoft.com/6910c51d-4176-49a3-be6b-6b072ad03fc1">FECMethod</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693580(v=VS.85).aspx">get_InnerFEC</a>



<a href="https://msdn.microsoft.com/library/Dd693586(v=VS.85).aspx">put_InnerFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693587(v=VS.85).aspx">put_OuterFEC</a>
 

 

