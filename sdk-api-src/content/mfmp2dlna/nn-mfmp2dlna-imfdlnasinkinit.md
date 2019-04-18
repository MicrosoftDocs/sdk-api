---
UID: NN:mfmp2dlna.IMFDLNASinkInit
title: IMFDLNASinkInit (mfmp2dlna.h)
author: windows-sdk-content
description: Initializes the Digital Living Network Alliance (DLNA) media sink.
old-location: mf\imfdlnasinkinit.htm
tech.root: medfound
ms.assetid: fec2933a-aa1a-41e5-b697-fdae548b3789
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFDLNASinkInit, IMFDLNASinkInit interface [Media Foundation], IMFDLNASinkInit interface [Media Foundation],described, mf.imfdlnasinkinit, mfmp2dlna/IMFDLNASinkInit
ms.topic: interface
req.header: mfmp2dlna.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - mfmp2dlna.h
api_name:
 - IMFDLNASinkInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDLNASinkInit interface


## -description


Initializes the Digital Living Network Alliance (DLNA) media sink. 

The DLNA media sink exposes this interface. To get a pointer to this interface, call <b>CoCreateInstance</b>. The CLSID is <b>CLSID_MPEG2DLNASink</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDLNASinkInit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDLNASinkInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDLNASinkInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48c3842c-7d88-4232-b882-363d9310ffe8">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the DLNA media sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

