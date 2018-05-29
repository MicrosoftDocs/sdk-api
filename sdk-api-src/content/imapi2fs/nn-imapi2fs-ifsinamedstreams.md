---
UID: NN:imapi2fs.IFsiNamedStreams
title: IFsiNamedStreams
author: windows-sdk-content
description: Use this interface to enumerate the named streams associated with a file in a file system image.
old-location: imapi\ifsinamedstreams.htm
old-project: imapi
ms.assetid: 383a83e4-5dc2-459a-a58f-b6ce7a656348
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFsiNamedStreams, IFsiNamedStreams interface [IMAPI], IFsiNamedStreams interface [IMAPI],described, imapi.ifsinamedstreams, imapi2fs/IFsiNamedStreams
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
req.idl: Imapi2.idl
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
-	IFsiNamedStreams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiNamedStreams interface


## -description


Use this interface to enumerate the named streams associated with a file in a file system image.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiNamedStreams</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsiNamedStreams</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsiNamedStreams</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d4efee2-607b-4be4-9854-79fed47503e4">get_Count</a>
</td>
<td align="left" width="63%">
Returns the number of the named streams associated with a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99691d12-bff6-4d75-b9ef-bd92f8198ae2">get_EnumNamedStreams</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IEnumFsiItems</b> list of named streams associated with a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5ab97cc-cc5a-4fc5-b79a-f1e0a8647c77">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a named stream associated with a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea1a14fe-91f0-4710-9d15-66a4c415f541">get_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IEnumVARIANT</b> list of the named streams associated with a file.

</td>
</tr>
</table> 


## -remarks



To access this interface, call the <a href="https://msdn.microsoft.com/011c6241-4989-41ca-9876-d6810797a382">IFsiFileItem2::get_FsiNamedStreams</a> method of a file item object representing a standard or 'Real-Time' file.

This interface is provided only for file item objects representing regular or 'Real-Time' files. Named streams cannot have other name streams associated with them.

UDF must be enabled and set to UDF revision 2.00 or later in order to enable named stream support.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/f35d1cd9-8a04-4c12-9af3-38f2c44b8c06">IFsiFileItem2</a>
 

 

