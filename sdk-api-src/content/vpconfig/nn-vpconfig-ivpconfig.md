---
UID: NN:vpconfig.IVPConfig
title: IVPConfig (vpconfig.h)
author: windows-sdk-content
description: The IVPConfig interface must be implemented by any filter that wraps a hardware decoder with a video port.
old-location: dshow\ivpconfig.htm
tech.root: DirectShow
ms.assetid: 2c0eb294-7e57-4d8d-98b1-57c3834279a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVPConfig, IVPConfig interface [DirectShow], IVPConfig interface [DirectShow],described, IVPConfigInterface, dshow.ivpconfig, vpconfig/IVPConfig
ms.topic: interface
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVPConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVPConfig interface


## -description



The <b>IVPConfig</b> interface must be implemented by any filter that wraps a hardware decoder with a video port. This enables the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>, through its <a href="https://msdn.microsoft.com/en-us/library/Dd390589(v=VS.85).aspx">IVPNotify</a> interface, to set and retrieve configuration information on the video port regarding the video memory on the display adapter. This interface derives from <a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig</a>.

Applications never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPConfig</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig</a>. <b>IVPConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390584(v=VS.85).aspx">IsVPDecimationAllowed</a>
</td>
<td align="left" width="63%">
Given the context, retrieves whether scaling at the video port is possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390585(v=VS.85).aspx">SetScalingFactors</a>
</td>
<td align="left" width="63%">
Sets the factors by which the decoder should scale the video stream.

</td>
</tr>
</table> 


## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390581(v=VS.85).aspx">IVPBaseNotify</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390590(v=VS.85).aspx">IVPNotify2</a>
 

 

