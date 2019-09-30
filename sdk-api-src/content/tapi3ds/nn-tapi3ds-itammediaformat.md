---
UID: NN:tapi3ds.ITAMMediaFormat
title: ITAMMediaFormat (tapi3ds.h)
author: windows-sdk-content
description: The ITAMMediaFormat interface sets and gets DirectShow media format.
old-location: tapi3\itammediaformat.htm
tech.root: Tapi
ms.assetid: 82728afe-5743-4b45-86e6-32df021a2a5f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAMMediaFormat, ITAMMediaFormat interface [TAPI 2.2], ITAMMediaFormat interface [TAPI 2.2],described, _tapi3_itammediaformat, tapi3.itammediaformat, tapi3ds/ITAMMediaFormat
ms.topic: interface
f1_keywords: 
 - "tapi3ds/ITAMMediaFormat"
req.header: tapi3ds.h
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
 - ITAMMediaFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAMMediaFormat interface


## -description


The 
<b>ITAMMediaFormat</b> interface sets and gets DirectShow media format. The format is described using the 
<b>AM_MEDIA_TYPE</b> structure. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. This interface is exposed on a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a> only if an MSP is involved in terminal creation and implements this interface. The 
<b>ITAMMediaFormat</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.

On addresses where a variety of formats are supported (such as Wave MSP addresses, which are used on most modems and voice boards), this media format must be set or the terminal will not be able to connect.

For other addresses, such as those implemented over IP, the format may be fixed/predetermined. In that case, a call to set format will fail if the format is not the same as the predetermined format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAMMediaFormat</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITAMMediaFormat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAMMediaFormat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat">get_MediaFormat</a>
</td>
<td align="left" width="63%">
Gets the media format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat">put_MediaFormat</a>
</td>
<td align="left" width="63%">
Sets the media format.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>
 

 

