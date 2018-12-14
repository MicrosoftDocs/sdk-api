---
UID: NF:msvidctl.IMSVidCtl.get_ColorKey
title: IMSVidCtl::get_ColorKey
author: windows-sdk-content
description: The get_ColorKey method retrieves the color key that the video renderer is using.
old-location: mstv\imsvidctl_get_colorkey.htm
tech.root: mstv
ms.assetid: 2f197faf-a91e-4984-8858-ceab6506b273
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_ColorKey method, IMSVidCtl.get_ColorKey, IMSVidCtl::get_ColorKey, IMSVidCtlget_ColorKey, get_ColorKey, get_ColorKey method [Microsoft TV Technologies], get_ColorKey method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_colorkey, msvidctl/IMSVidCtl::get_ColorKey
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
 - IMSVidCtl.get_ColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get_ColorKey


## -description


The <b>get_ColorKey</b> method retrieves the color key that the video renderer is using.


## -parameters




### -param CurrentValue [out]

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



<a href="https://msdn.microsoft.com/en-us/library/Dd390554(v=VS.85).aspx">IVMRWindowlessControl::GetColorKey</a>
 

 

