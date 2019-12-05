---
UID: NN:mfsharingengine.IPlayToSourceClassFactory
title: IPlayToSourceClassFactory (mfsharingengine.h)
description: Creates an instance of the PlayToSource object.
old-location: mf\iplaytosourceclassfactory.htm
tech.root: medfound
ms.assetid: F8F9FEC6-836C-429A-BADD-5CD1E550AED0
ms.date: 12/05/2018
ms.keywords: IPlayToSourceClassFactory, IPlayToSourceClassFactory interface [Media Foundation], IPlayToSourceClassFactory interface [Media Foundation],described, mf.iplaytocontrollerclassfactory, mf.iplaytosourceclassfactory, mfsharingengine/IPlayToSourceClassFactory
ms.topic: interface
f1_keywords:
- mfsharingengine/IPlayToSourceClassFactory
dev_langs:
- c++
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- mfsharingengine.h
api_name:
- IPlayToSourceClassFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPlayToSourceClassFactory interface


## -description


Creates an instance of the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.media.playto.playtosource">PlayToSource</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlayToSourceClassFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPlayToSourceClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPlayToSourceClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfsharingengine/nf-mfsharingengine-iplaytosourceclassfactory-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of the <b>PlayToController</b> object.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. The CLSID is <b>CLSID_PlayToSourceClassFactory</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

