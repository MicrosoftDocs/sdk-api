---
UID: NF:msvidctl.IMSVidCtl.get_ColorKey
title: IMSVidCtl::get_ColorKey method
author: windows-driver-content
description: The get_ColorKey method retrieves the color key that the video renderer is using.
old-location: mstv\imsvidctl_get_colorkey.htm
old-project: mstv
ms.assetid: 2f197faf-a91e-4984-8858-ceab6506b273
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], get_ColorKey method, IMSVidCtl::get_ColorKey, IMSVidCtlget_ColorKey, get_ColorKey method [Microsoft TV Technologies], get_ColorKey method [Microsoft TV Technologies], IMSVidCtl interface, get_ColorKey,IMSVidCtl.get_ColorKey, mstv.imsvidctl_get_colorkey, msvidctl/IMSVidCtl::get_ColorKey
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.get_ColorKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidCtl::get_ColorKey method


## -description


The <b>get_ColorKey</b> method retrieves the color key that the video renderer is using.


## -parameters




### -param CurrentValue






#### - pCurrentValue [out]

Receives an <b>OLE_COLOR</b> value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The color key is used when the video renderer draws to an overlay surface.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
OLE_COLOR ocKey;
COLORREF clrKey;
pVideoControl-&gt;get_ColorKey(&amp;ocKey);
OleTranslateColor(ocKey, 0, &amp;clrKey);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/2896f062-4ff9-4652-89b9-5fe55c6fe472">IMSVidCtl::put_ColorKey</a>



<a href="https://msdn.microsoft.com/e10f9e03-fbcd-4002-babc-fb028e399d72">IVMRWindowlessControl::GetColorKey</a>
 

 

