---
UID: NF:tuner.ILocator.put_OuterFECRate
title: ILocator::put_OuterFECRate (tuner.h)
author: windows-sdk-content
description: The put_OuterFECRate method sets the outer FEC rate.
old-location: mstv\ilocator_put_outerfecrate.htm
tech.root: mstv
ms.assetid: 0fd3fa42-4ed6-459b-a6a2-23ed67832780
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorput_OuterFECRate, ILocator interface [Microsoft TV Technologies],put_OuterFECRate method, ILocator.put_OuterFECRate, ILocator::put_OuterFECRate, mstv.ilocator_put_outerfecrate, put_OuterFECRate, put_OuterFECRate method [Microsoft TV Technologies], put_OuterFECRate method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_OuterFECRate
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
 - ILocator.put_OuterFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocator::put_OuterFECRate


## -description



The <b>put_OuterFECRate</b> method sets the outer FEC rate.




## -parameters




### -param FEC [in]

Specifies the outer FEC rate. This parameter is a value of type <a href="https://msdn.microsoft.com/161c963f-55b2-4a17-a537-47de3326df0e">BinaryConvolutionCodeRate</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/library/Dd693583(v=VS.85).aspx">get_OuterFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693586(v=VS.85).aspx">put_InnerFECRate</a>



<a href="https://msdn.microsoft.com/library/Dd693587(v=VS.85).aspx">put_OuterFEC</a>
 

 

