---
UID: NN:objidl.IInitializeSpy
title: IInitializeSpy (objidl.h)
author: windows-sdk-content
description: Performs initialization or cleanup when entering or exiting a COM apartment.
old-location: com\iinitializespy.htm
tech.root: com
ms.assetid: 9cf1a3fa-dbc6-4760-a9e9-ef237737acfb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInitializeSpy, IInitializeSpy interface [COM], IInitializeSpy interface [COM],described, _com_iinitializespy, com.iinitializespy, objidl/IInitializeSpy
ms.topic: interface
f1_keywords: 
 - "objidl/IInitializeSpy"
req.header: objidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInitializeSpy interface


## -description


Performs initialization or cleanup when entering or exiting a COM apartment.
 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeSpy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeSpy</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iinitializespy-postinitialize">PostInitialize</a>
</td>
<td align="left" width="63%">
Performs initialization steps required after calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iinitializespy-postuninitialize">PostUninitialize</a>
</td>
<td align="left" width="63%">
Performs cleanup steps required after calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iinitializespy-preinitialize">PreInitialize</a>
</td>
<td align="left" width="63%">
Performs initialization steps required before calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iinitializespy-preuninitialize">PreUninitialize</a>
</td>
<td align="left" width="63%">
Performs cleanup steps required before calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> function.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregisterinitializespy">CoRegisterInitializeSpy</a>
 

 

