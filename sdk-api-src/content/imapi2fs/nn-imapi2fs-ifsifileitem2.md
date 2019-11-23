---
UID: NN:imapi2fs.IFsiFileItem2
title: IFsiFileItem2 (imapi2fs.h)

description: Use this interface to add, remove and enumerate named streams associated with a file. This interface also provides access to the 'Real-Time' attribute of a file.
old-location: imapi\ifsifileitem2.htm
tech.root: imapi
ms.assetid: f35d1cd9-8a04-4c12-9af3-38f2c44b8c06

ms.date: 12/05/2018
ms.keywords: IFsiFileItem2, IFsiFileItem2 interface [IMAPI], IFsiFileItem2 interface [IMAPI],described, imapi.ifsifileitem2, imapi2fs/IFsiFileItem2
ms.topic: interface
f1_keywords: 
 - "imapi2fs/IFsiFileItem2"
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
req.idl: Imapi2.idl
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
 - IFsiFileItem2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsiFileItem2 interface


## -description


Use this interface to add, remove and enumerate named streams associated with a file. This interface also provides  access to the 'Real-Time' attribute of a file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiFileItem2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>. <b>IFsiFileItem2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsiFileItem2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Associates a named stream with a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-get_fsinamedstreams">get_FsiNamedStreams</a>
</td>
<td align="left" width="63%">
Retrieves the named streams associated with a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-get_isnamedstream">get_IsNamedStream</a>
</td>
<td align="left" width="63%">
Determines if the item is a named stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-get_isrealtime">get_IsRealTime</a>
</td>
<td align="left" width="63%">
Determines if a file item is a 'Real-Time' or a standard file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-put_isrealtime">put_IsRealTime</a>
</td>
<td align="left" width="63%">
Sets the 'Real-Time' attribute of a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem2-removestream">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a named stream association with a file.

</td>
</tr>
</table> 


## -remarks



While UDF 2.0 is the lowest required revision for named stream support, the user must enable UDF  2.01 or higher to enable the use of both named streams and   real-time file attributes.


The recipients of a storage medium containing such files are required to read them using special MMC commands reducing read latency and increasing the worst-case read speed.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<b></b>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>
 

 

