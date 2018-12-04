---
UID: NF:msvidctl.IMSVidCtl.get_InputsAvailable
title: IMSVidCtl::get_InputsAvailable
author: windows-sdk-content
description: The get_InputsAvailable method retrieves the input devices that are available within a specified category.
old-location: mstv\imsvidctl_get_inputsavailable.htm
tech.root: mstv
ms.assetid: 7ed22c3e-745a-4680-a5fc-accef56ab348
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_InputsAvailable method, IMSVidCtl.get_InputsAvailable, IMSVidCtl::get_InputsAvailable, IMSVidCtlget_InputsAvailable, get_InputsAvailable, get_InputsAvailable method [Microsoft TV Technologies], get_InputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_inputsavailable, msvidctl/IMSVidCtl::get_InputsAvailable
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
 - IMSVidCtl.get_InputsAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get_InputsAvailable


## -description


The <b>get_InputsAvailable</b> method retrieves the input devices that are available within a specified category.


## -parameters




### -param CategoryGuid [in]

<b>BSTR</b> that specifies the GUID of the category to enumerate.


### -param pVal [out]

Receives an <a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is provided for Automation clients. C++ applications can use the <a href="https://msdn.microsoft.com/2d77eca3-aec9-423d-8d02-92e6f9ab5167">IMSVidCtl::get__InputsAvailable</a> method, which takes a GUID rather than a <b>BSTR</b> value.

If the method succeeds, the <a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>
 

 

