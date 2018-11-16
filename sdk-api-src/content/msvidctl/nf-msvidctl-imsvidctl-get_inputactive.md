---
UID: NF:msvidctl.IMSVidCtl.get_InputActive
title: IMSVidCtl::get_InputActive
author: windows-sdk-content
description: The get_InputActive method retrieves the input device that is currently active.
old-location: mstv\imsvidctl_get_inputactive.htm
tech.root: mstv
ms.assetid: 3451002b-5339-4b43-aefd-d66c48f7ae57
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_InputActive method, IMSVidCtl.get_InputActive, IMSVidCtl::get_InputActive, IMSVidCtlget_InputActive, get_InputActive, get_InputActive method [Microsoft TV Technologies], get_InputActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_inputactive, msvidctl/IMSVidCtl::get_InputActive
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMSVidCtl.get_InputActive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msvidctl.h
: 
- IMSVidCtl.get_InputActive
: 
---

# IMSVidCtl::get_InputActive


## -description


The <b>get_InputActive</b> method retrieves the input device that is currently active.


## -parameters




### -param pVal [out]

Receives an <a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/696d8ece-a377-4fe8-a790-a68d1a24e65a">IMSVidCtl::put_InputActive</a>
 

 

