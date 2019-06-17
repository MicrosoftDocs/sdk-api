---
UID: NN:vss.IVssEnumObject
title: IVssEnumObject (vss.h)
author: windows-sdk-content
description: Contains methods to iterate over and perform other operations on a list of enumerated objects.
old-location: base\ivssenumobject.htm
tech.root: VSS
ms.assetid: b8e80909-a28a-45d7-87e2-4f44bf6990f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssEnumObject, IVssEnumObject interface [VSS], IVssEnumObject interface [VSS],described, _win32_ivssenumobject, base.ivssenumobject, vss/IVssEnumObject
ms.topic: interface
f1_keywords: ["vss/IVssEnumObject"]
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssEnumObject interface


## -description


The <b>IVssEnumObject</b> interface contains methods 
    to iterate over and perform other operations on a list of enumerated objects.

The calling application is responsible for calling 
    <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources held by the 
    returned <b>IVssEnumObject</b> when it is no longer needed. It 
    may also need to call <b>IUnknown::Release</b> to release 
    temporary objects (such as strings) returned during enumeration.

The <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a> method 
    returns an <b>IVssEnumObject</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssEnumObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssEnumObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssEnumObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssenumobject-clone">Clone</a>
</td>
<td align="left" width="63%">
Copies the specified list of enumerated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssenumobject-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next specified number of objects from the list of enumerated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssenumobject-reset">Reset</a>
</td>
<td align="left" width="63%">
Clears the list of enumerated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssenumobject-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of objects in the list of enumerated objects.

</td>
</tr>
</table> 

