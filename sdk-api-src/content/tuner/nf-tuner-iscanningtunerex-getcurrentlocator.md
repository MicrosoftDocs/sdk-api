---
UID: NF:tuner.IScanningTunerEx.GetCurrentLocator
title: IScanningTunerEx::GetCurrentLocator
author: windows-sdk-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_getcurrentlocator.htm
tech.root: mstv
ms.assetid: f5237236-50f3-49dd-aec0-578e0a8430c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentLocator, GetCurrentLocator method [Microsoft TV Technologies], GetCurrentLocator method [Microsoft TV Technologies],IScanningTunerEx interface, IScanningTunerEx interface [Microsoft TV Technologies],GetCurrentLocator method, IScanningTunerEx.GetCurrentLocator, IScanningTunerEx::GetCurrentLocator, IScanningTunerExGetCurrentLocator, mstv.iscanningtunerex_getcurrentlocator, tuner/IScanningTunerEx::GetCurrentLocator
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Tuner.h
api_name:
 - IScanningTunerEx.GetCurrentLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScanningTunerEx::GetCurrentLocator


## -description



This topic applies to Windows Vista and later.
        



The <b>GetCurrentLocator</b> method retrieves the current locator object.


## -parameters




### -param pILocator [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> interface of the locator object. The caller must release the interface.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

