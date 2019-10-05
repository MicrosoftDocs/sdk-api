---
UID: NN:shobjidl.IAccessibleObject
title: IAccessibleObject (shobjidl.h)
author: windows-sdk-content
description: Exposes a method that can be used by an accessibility application.
old-location: shell\IAccessibleObject.htm
tech.root: shell
ms.assetid: bac49a2d-4357-4607-a89d-d2ed4abf89bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccessibleObject, IAccessibleObject interface [Windows Shell], IAccessibleObject interface [Windows Shell],described, _shell_IAccessibleObject, shell.IAccessibleObject, shobjidl/IAccessibleObject
ms.topic: interface
f1_keywords: 
 - "shobjidl/IAccessibleObject"
dev_langs:
 - c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - IAccessibleObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessibleObject interface


## -description


Exposes a method that can be used by an accessibility application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccessibleObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibleobject-setaccessiblename">SetAccessibleName</a>
</td>
<td align="left" width="63%">
Sets text that is retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accname">IAccessible::get_accName</a> which accessibility tools use to obtain the Name Property of an object.


</td>
</tr>
</table> 

