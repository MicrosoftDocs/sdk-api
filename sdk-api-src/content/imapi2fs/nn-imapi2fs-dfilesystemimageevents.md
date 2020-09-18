---
UID: NN:imapi2fs.DFileSystemImageEvents
title: DFileSystemImageEvents (imapi2fs.h)
description: Implement this interface to receive notifications of the current write operation.
helpviewer_keywords: ["DFileSystemImageEvents","DFileSystemImageEvents interface [IMAPI]","DFileSystemImageEvents interface [IMAPI]","described","imapi.dfilesystemimageevents","imapi2fs/DFileSystemImageEvents"]
old-location: imapi\dfilesystemimageevents.htm
tech.root: imapi
ms.assetid: cff27ceb-d14a-48c2-941e-d27d6505e2c5
ms.date: 12/05/2018
ms.keywords: DFileSystemImageEvents, DFileSystemImageEvents interface [IMAPI], DFileSystemImageEvents interface [IMAPI],described, imapi.dfilesystemimageevents, imapi2fs/DFileSystemImageEvents
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DFileSystemImageEvents
 - imapi2fs/DFileSystemImageEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - DFileSystemImageEvents
---

# DFileSystemImageEvents interface


## -description

Implement this interface to receive notifications of the current write operation.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DFileSystemImageEvents</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>DFileSystemImageEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DFileSystemImageEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-dfilesystemimageevents-update">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current write operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>