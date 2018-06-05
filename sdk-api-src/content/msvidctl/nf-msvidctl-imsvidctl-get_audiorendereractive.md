---
UID: NF:msvidctl.IMSVidCtl.get_AudioRendererActive
title: IMSVidCtl::get_AudioRendererActive
author: windows-sdk-content
description: The get_AudioRendererActive method retrieves the audio renderer that is currently active.
old-location: mstv\imsvidctl_get_audiorendereractive.htm
old-project: mstv
ms.assetid: 4ac78904-18ca-4bcb-9c0e-15595a756ecd
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_AudioRendererActive method, IMSVidCtl.get_AudioRendererActive, IMSVidCtl::get_AudioRendererActive, IMSVidCtlget_AudioRendererActive, get_AudioRendererActive, get_AudioRendererActive method [Microsoft TV Technologies], get_AudioRendererActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_audiorendereractive, msvidctl/IMSVidCtl::get_AudioRendererActive
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.get_AudioRendererActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::get_AudioRendererActive


## -description


The <b>get_AudioRendererActive</b> method retrieves the audio renderer that is currently active.


## -parameters




### -param pVal






#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer</a> interface pointer. The caller must release the interface. If no audio renderer is active, this parameter receives the value <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/1f6498ce-fb53-4d57-b6bd-6696ba57de3b">IMSVidCtl::put_AudioRendererActive</a>
 

 

