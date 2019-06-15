---
UID: NN:mfidl.IMFTimer
title: IMFTimer (mfidl.h)
author: windows-sdk-content
description: Provides a timer that invokes a callback at a specified time.
old-location: mf\imftimer.htm
tech.root: medfound
ms.assetid: 152594df-de3d-4f6f-9277-dba95ab3533a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 152594df-de3d-4f6f-9277-dba95ab3533a, IMFTimer, IMFTimer interface [Media Foundation], IMFTimer interface [Media Foundation],described, mf.imftimer, mfidl/IMFTimer
ms.topic: interface
f1_keywords: ["mfidl/IMFTimer"]
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimer interface


## -description


Provides a timer that invokes a callback at a specified time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftimer-canceltimer">CancelTimer</a>
</td>
<td align="left" width="63%">
Cancels a timer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftimer-settimer">SetTimer</a>
</td>
<td align="left" width="63%">
Sets a timer that invokes a callback.
        

</td>
</tr>
</table> 


## -remarks



The presentation clock exposes this interface. To get a pointer to the interface, call <b>QueryInterface</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
 

 

