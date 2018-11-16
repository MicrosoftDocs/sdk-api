---
UID: NN:segment.IMSVidXDS
title: IMSVidXDS
author: windows-sdk-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. The IMSVidXDS interface provides access to the extended data services. The MSVidXDS feature exposes this interface.
old-location: mstv\imsvidxds.htm
tech.root: mstv
ms.assetid: ddd172fe-2f93-4b1b-b325-81be024bf74c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidXDS, IMSVidXDS interface [Microsoft TV Technologies], IMSVidXDS interface [Microsoft TV Technologies],described, IMSVidXDSInterface, mstv.imsvidxds, segment/IMSVidXDS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidXDS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidXDS interface


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>


The <b>IMSVidXDS</b> interface provides access to the extended data services. The <a href="https://msdn.microsoft.com/30b9709e-8f37-4b74-ad96-6da48efaff32">MSVidXDS</a> feature exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidXDS</b> interface inherits from <a href="https://msdn.microsoft.com/0512e1d6-e10e-421e-846c-4bcd7e86d0e7">IMSVidFeature</a>. <b>IMSVidXDS</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidXDS</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/078bd274-b8dc-425b-b14f-3dacff6744bb">get_ChannelChangeInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the channel change interface.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidXDS)</code>.




## -see-also




<a href="https://msdn.microsoft.com/0512e1d6-e10e-421e-846c-4bcd7e86d0e7">IMSVidFeature</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

