---
UID: NF:msvidctl.IMSVidCtl.get_OutputsActive
title: IMSVidCtl::get_OutputsActive (msvidctl.h)
author: windows-sdk-content
description: The get_OutputsActive method retrieves the output devices that are currently active.
old-location: mstv\imsvidctl_get_outputsactive.htm
tech.root: mstv
ms.assetid: 9465ff38-c524-47e1-8bc0-bd6b2e0dea8c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_OutputsActive method, IMSVidCtl.get_OutputsActive, IMSVidCtl::get_OutputsActive, IMSVidCtlget_OutputsActive, get_OutputsActive, get_OutputsActive method [Microsoft TV Technologies], get_OutputsActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_outputsactive, msvidctl/IMSVidCtl::get_OutputsActive
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
 - IMSVidCtl.get_OutputsActive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidCtl::get_OutputsActive


## -description


The <b>get_OutputsActive</b> method retrieves the output devices that are currently active.


## -parameters




### -param pVal [out]

Receives an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidoutputdevices">IMSVidOutputDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">IMSVidCtl::get_AudioRendererActive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorendereractive">IMSVidCtl::get_VideoRendererActive</a>
 

 

