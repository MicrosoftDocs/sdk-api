---
UID: NF:msvidctl.IMSVidCtl.put_InputActive
title: IMSVidCtl::put_InputActive
author: windows-sdk-content
description: The put_InputActive method specifies the input device to use in the filter graph.
old-location: mstv\imsvidctl_put_inputactive.htm
old-project: mstv
ms.assetid: 696d8ece-a377-4fe8-a790-a68d1a24e65a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_InputActive method, IMSVidCtl.put_InputActive, IMSVidCtl::put_InputActive, IMSVidCtlput_InputActive, mstv.imsvidctl_put_inputactive, msvidctl/IMSVidCtl::put_InputActive, put_InputActive, put_InputActive method [Microsoft TV Technologies], put_InputActive method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.put_InputActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::put_InputActive


## -description


The <b>put_InputActive</b> method specifies the input device to use in the filter graph.


## -parameters




### -param pVal [in]

Specifies a pointer to the input device's <a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the Video Control's state is not <b>STATE_UNBUILT</b>, call the <a href="https://msdn.microsoft.com/e67bf380-dc2c-42c9-a995-17951c65fbda">IMSVidCtl::Decompose</a> to tear down the filter graph before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/3451002b-5339-4b43-aefd-d66c48f7ae57">IMSVidCtl::get_InputActive</a>



<a href="https://msdn.microsoft.com/45f35832-709c-4f78-9e1a-a6ad489fc81f">IMSVidCtl::get_State</a>
 

 

