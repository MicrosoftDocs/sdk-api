---
UID: NF:msvidctl.IMSVidCtl.put_AudioRendererActive
title: IMSVidCtl::put_AudioRendererActive
author: windows-sdk-content
description: The put_AudioRendererActive method specifies the active audio renderer.
old-location: mstv\imsvidctl_put_audiorendereractive.htm
old-project: mstv
ms.assetid: 1f6498ce-fb53-4d57-b6bd-6696ba57de3b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_AudioRendererActive method, IMSVidCtl.put_AudioRendererActive, IMSVidCtl::put_AudioRendererActive, IMSVidCtlput_AudioRendererActive, mstv.imsvidctl_put_audiorendereractive, msvidctl/IMSVidCtl::put_AudioRendererActive, put_AudioRendererActive, put_AudioRendererActive method [Microsoft TV Technologies], put_AudioRendererActive method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.redist: 
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
 - IMSVidCtl.put_AudioRendererActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::put_AudioRendererActive


## -description


The <b>put_AudioRendererActive</b> method specifies the active audio renderer.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer</a> interface that specifies the audio renderer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/4ac78904-18ca-4bcb-9c0e-15595a756ecd">IMSVidCtl::get_AudioRendererActive</a>
 

 

