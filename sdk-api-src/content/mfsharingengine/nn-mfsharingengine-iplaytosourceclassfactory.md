---
UID: NN:mfsharingengine.IPlayToSourceClassFactory
title: IPlayToSourceClassFactory (mfsharingengine.h)
author: windows-sdk-content
description: Creates an instance of the PlayToSource object.
old-location: mf\iplaytosourceclassfactory.htm
tech.root: medfound
ms.assetid: F8F9FEC6-836C-429A-BADD-5CD1E550AED0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPlayToSourceClassFactory, IPlayToSourceClassFactory interface [Media Foundation], IPlayToSourceClassFactory interface [Media Foundation],described, mf.iplaytocontrollerclassfactory, mf.iplaytosourceclassfactory, mfsharingengine/IPlayToSourceClassFactory
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPlayToSourceClassFactory interface


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/3c125341-5b2e-4da0-b6c9-def4478e3be2">PlayToSource</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlayToSourceClassFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPlayToSourceClassFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3F7F8441-B0A2-407E-B127-C7DC66CA34DE">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of the <b>PlayToController</b> object.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>. The CLSID is <b>CLSID_PlayToSourceClassFactory</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

