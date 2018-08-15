---
UID: NN:objidl.IInitializeSpy
title: IInitializeSpy
author: windows-sdk-content
description: Performs initialization or cleanup when entering or exiting a COM apartment.
old-location: com\iinitializespy.htm
old-project: com
ms.assetid: 9cf1a3fa-dbc6-4760-a9e9-ef237737acfb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInitializeSpy, IInitializeSpy interface [COM], IInitializeSpy interface [COM],described, _com_iinitializespy, com.iinitializespy, objidl/IInitializeSpy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IInitializeSpy
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IInitializeSpy interface


## -description


Performs initialization or cleanup when entering or exiting a COM apartment.
 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeSpy</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IInitializeSpy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeSpy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdef4089-93e6-4845-8dcc-1150d7a0d033">PostInitialize</a>
</td>
<td align="left" width="63%">
Performs initialization steps required after calling the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f91a1a4a-4d0b-491e-a7c6-01596b5b9712">PostUninitialize</a>
</td>
<td align="left" width="63%">
Performs cleanup steps required after calling the <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5b345d1-ab37-401a-9cb4-b01ef7254fc8">PreInitialize</a>
</td>
<td align="left" width="63%">
Performs initialization steps required before calling the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22f9c663-0c6e-4413-a3a3-21cbb5ce62c9">PreUninitialize</a>
</td>
<td align="left" width="63%">
Performs cleanup steps required before calling the <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> function.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1fd5606e-0a15-429a-b656-4620b873bec5">CoRegisterInitializeSpy</a>
 

 

