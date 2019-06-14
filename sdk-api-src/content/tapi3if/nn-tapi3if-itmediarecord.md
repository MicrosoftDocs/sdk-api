---
UID: NN:tapi3if.ITMediaRecord
title: ITMediaRecord (tapi3if.h)
author: windows-sdk-content
description: The ITMediaRecord interface provides recording-specific methods that allow an application to set and get the names of files to record.
old-location: tapi3\itmediarecord.htm
tech.root: Tapi
ms.assetid: 604b0128-1461-40f2-98fe-801dbb71e005
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITMediaRecord, ITMediaRecord interface [TAPI 2.2], ITMediaRecord interface [TAPI 2.2],described, _tapi3_itmediarecord, tapi3.itmediarecord, tapi3if/ITMediaRecord
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMediaRecord interface


## -description


The 
<b>ITMediaRecord</b> interface provides recording-specific methods that allow an application to set and get the names of files to record.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaRecord</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITMediaRecord</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMediaRecord</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediarecord-get_filename">get_FileName</a>
</td>
<td align="left" width="63%">
Gets the name of the file used for recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediarecord-put_filename">put_FileName</a>
</td>
<td align="left" width="63%">
Sets the name of the file to record.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback">ITMediaPlayback</a>
 

 

