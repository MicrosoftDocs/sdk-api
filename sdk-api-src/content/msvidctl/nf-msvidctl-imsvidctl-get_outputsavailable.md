---
UID: NF:msvidctl.IMSVidCtl.get_OutputsAvailable
title: IMSVidCtl::get_OutputsAvailable
author: windows-sdk-content
description: The get_OutputsAvailable method retrieves the output devices that are available in a specified category.
old-location: mstv\imsvidctl_get_outputsavailable.htm
tech.root: mstv
ms.assetid: f45b752c-6b7f-4803-93fe-92ec44cd9509
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_OutputsAvailable method, IMSVidCtl.get_OutputsAvailable, IMSVidCtl::get_OutputsAvailable, IMSVidCtlget_OutputsAvailable, get_OutputsAvailable, get_OutputsAvailable method [Microsoft TV Technologies], get_OutputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_outputsavailable, msvidctl/IMSVidCtl::get_OutputsAvailable
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - msvidctl.h
api_name:
 - IMSVidCtl.get_OutputsAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get_OutputsAvailable


## -description


The <b>get_OutputsAvailable</b> method retrieves the output devices that are available in a specified category.


## -parameters




### -param CategoryGuid [in]

<b>BSTR</b> that specifies the GUID of the category to enumerate


### -param pVal [out]

Receives an <a href="https://msdn.microsoft.com/54776225-ad60-450b-99b4-851cae60ffa7">IMSVidOutputDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/6ab81536-2701-408e-be3a-f44375ef8193">IMSVidCtl::get_AudioRenderersAvailable</a>



<a href="https://msdn.microsoft.com/20e5b2f3-33ea-4b0d-84b8-e4b0b61e0348">IMSVidCtl::get_VideoRenderersAvailable</a>
 

 

