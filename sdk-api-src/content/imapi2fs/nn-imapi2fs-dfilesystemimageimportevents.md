---
UID: NN:imapi2fs.DFileSystemImageImportEvents
title: DFileSystemImageImportEvents (imapi2fs.h)
description: Use this interface to receives notifications regarding the current file system import operation.
helpviewer_keywords: ["DFileSystemImageImportEvents","DFileSystemImageImportEvents interface [IMAPI]","DFileSystemImageImportEvents interface [IMAPI]","described","imapi.dfilesystemimageimportevents","imapi2fs/DFileSystemImageImportEvents"]
old-location: imapi\dfilesystemimageimportevents.htm
tech.root: imapi
ms.assetid: 972ab985-17c5-4458-a7f4-59ac25c0dca4
ms.date: 12/05/2018
ms.keywords: DFileSystemImageImportEvents, DFileSystemImageImportEvents interface [IMAPI], DFileSystemImageImportEvents interface [IMAPI],described, imapi.dfilesystemimageimportevents, imapi2fs/DFileSystemImageImportEvents
f1_keywords:
- imapi2fs/DFileSystemImageImportEvents
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
- DFileSystemImageImportEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DFileSystemImageImportEvents interface


## -description


Use this interface to receives notifications regarding the current file system import operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DFileSystemImageImportEvents</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>DFileSystemImageImportEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DFileSystemImageImportEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-dfilesystemimageimportevents-updateimport">UpdateImport</a>
</td>
<td align="left" width="63%">
When implemented, receives import notification for every file and directory item imported from an optical medium.

</td>
</tr>
</table> 


## -remarks



This interface supports import notifications for ISO9660, Joliet and UDF file systems.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

