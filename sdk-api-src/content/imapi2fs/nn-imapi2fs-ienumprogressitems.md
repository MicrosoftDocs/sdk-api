---
UID: NN:imapi2fs.IEnumProgressItems
title: IEnumProgressItems (imapi2fs.h)
author: windows-sdk-content
description: Use this interface to enumerate a collection of progress items.
old-location: imapi\ienumprogressitems.htm
tech.root: imapi
ms.assetid: c4238fbe-762a-492f-9eb5-d927e64436e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumProgressItems, IEnumProgressItems interface [IMAPI], IEnumProgressItems interface [IMAPI],described, imapi.ienumprogressitems, imapi2fs/IEnumProgressItems
ms.topic: interface
f1_keywords: 
 - "imapi2fs/IEnumProgressItems"
dev_langs:
 - c++
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - IEnumProgressItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumProgressItems interface


## -description


Use this interface to enumerate a collection of progress items.

To get this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-get_enumprogressitems">IProgressItems::get_EnumProgressItems</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumProgressItems</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumProgressItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumProgressItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/imapi/ienumprogressitems-remotenext">RemoteNext</a>
</td>
<td align="left" width="63%">
Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



This is a <b>EnumProgressItems</b> object in script.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>
 

 

