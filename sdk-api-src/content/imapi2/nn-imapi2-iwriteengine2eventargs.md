---
UID: NN:imapi2.IWriteEngine2EventArgs
title: IWriteEngine2EventArgs (imapi2.h)
author: windows-sdk-content
description: Use this interface to retrieve information about the current write operation. This interface is passed to the DWriteEngine2Events::Update method that you implement.
old-location: imapi\iwriteengine2eventargs.htm
tech.root: imapi
ms.assetid: 1922410a-5871-477f-b778-36b12ad95168
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWriteEngine2EventArgs, IWriteEngine2EventArgs interface [IMAPI], IWriteEngine2EventArgs interface [IMAPI],described, imapi.iwriteengine2eventargs, imapi2/IWriteEngine2EventArgs
ms.topic: interface
f1_keywords: 
 - "imapi2/IWriteEngine2EventArgs"
dev_langs:
 - c++
req.header: imapi2.h
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
 - imapi2.h
api_name:
 - IWriteEngine2EventArgs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWriteEngine2EventArgs interface


## -description


Use this interface to retrieve information about the current write operation. This interface is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-dwriteengine2events-update">DWriteEngine2Events::Update</a> method that you implement.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWriteEngine2EventArgs</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWriteEngine2EventArgs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWriteEngine2EventArgs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_freesystembuffer">get_FreeSystemBuffer</a>
</td>
<td align="left" width="63%">
Retrieves the number of unused bytes in the internal data buffer that is used for writing to disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_lastreadlba">get_LastReadLba</a>
</td>
<td align="left" width="63%">
Retrieves the address of the sector most recently read from the burn image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_lastwrittenlba">get_LastWrittenLba</a>
</td>
<td align="left" width="63%">
Retrieves the address of the sector most recently written to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_sectorcount">get_SectorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of sectors to write to the device in the current write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_startlba">get_StartLba</a>
</td>
<td align="left" width="63%">
Retrieves the starting logical block address (LBA) of the current write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_totalsystembuffer">get_TotalSystemBuffer</a>
</td>
<td align="left" width="63%">
Retrieves the size of the internal data buffer that is used for writing to disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_usedsystembuffer">get_UsedSystemBuffer</a>
</td>
<td align="left" width="63%">
Retrieves the number of used bytes in the internal data buffer that is used for writing to disc.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>
 

 

