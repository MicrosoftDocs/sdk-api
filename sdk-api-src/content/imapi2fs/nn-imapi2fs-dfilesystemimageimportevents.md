---
UID: NN:imapi2fs.DFileSystemImageImportEvents
title: DFileSystemImageImportEvents
author: windows-sdk-content
description: Use this interface to receives notifications regarding the current file system import operation.
old-location: imapi\dfilesystemimageimportevents.htm
old-project: imapi
ms.assetid: 972ab985-17c5-4458-a7f4-59ac25c0dca4
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: DFileSystemImageImportEvents, DFileSystemImageImportEvents interface [IMAPI], DFileSystemImageImportEvents interface [IMAPI],described, imapi.dfilesystemimageimportevents, imapi2fs/DFileSystemImageImportEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - DFileSystemImageImportEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DFileSystemImageImportEvents interface


## -description


Use this interface to receives notifications regarding the current file system import operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DFileSystemImageImportEvents</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>DFileSystemImageImportEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/83617039-686d-4c03-9f43-02ecde2ca53e">UpdateImport</a>
</td>
<td align="left" width="63%">
When implemented, receives import notification for every file and directory item imported from an optical medium.

</td>
</tr>
</table> 


## -remarks



This interface supports import notifications for ISO9660, Joliet and UDF file systems.




## -see-also




<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

