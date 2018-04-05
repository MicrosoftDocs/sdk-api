---
UID: NN:imapi2fs.IFsiDirectoryItem2
title: IFsiDirectoryItem2
author: windows-driver-content
description: Use this interface to add a directory tree, which includes all sub-directories, files, and associated named streams to a file system image.
old-location: imapi\ifsidirectoryitem2.htm
old-project: imapi
ms.assetid: fed2a858-d710-46be-a05b-dce7ef484636
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IFsiDirectoryItem2, IFsiDirectoryItem2 interface [IMAPI], IFsiDirectoryItem2 interface [IMAPI], described, imapi.ifsidirectoryitem2, imapi2fs/IFsiDirectoryItem2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFsiDirectoryItem2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiDirectoryItem2 interface


## -description


Use this interface to add a directory tree, which includes all sub-directories, files, and associated named streams to a file system image.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiDirectoryItem2</b> interface inherits from <a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>. <b>IFsiDirectoryItem2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsiDirectoryItem2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d87d1932-85d4-4d7d-99a7-933a87b48b6a">AddTreeWithNamedStreams</a>
</td>
<td align="left" width="63%">
Adds the contents of a directory tree along with the named streams associated with the files in the file system image.

</td>
</tr>
</table> 


## -remarks



All sub-directories, files, and associated named streams can only be added after the directory item has been  added to the file system image.

UDF must be enabled and set to UDF revision 2.00 or later in order to enable named stream support during the creation of the file system image.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>
 

 

