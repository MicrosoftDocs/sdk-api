---
UID: NN:amparse.IAMParse
title: IAMParse (amparse.h)
description: The IAMParse interface sets and retrieves the parse time for an MPEG-2 stream.
helpviewer_keywords: ["IAMParse","IAMParse interface [DirectShow]","IAMParse interface [DirectShow]","described","IAMParseInterface","amparse/IAMParse","dshow.iamparse"]
old-location: dshow\iamparse.htm
tech.root: dshow
ms.assetid: c5f3e153-c92f-4cdf-9aae-336b1f3dd8d6
ms.date: 12/05/2018
ms.keywords: IAMParse, IAMParse interface [DirectShow], IAMParse interface [DirectShow],described, IAMParseInterface, amparse/IAMParse, dshow.iamparse
req.header: amparse.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMParse
 - amparse/IAMParse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMParse
---

# IAMParse interface


## -description

The <code>IAMParse</code> interface sets and retrieves the <i>parse time</i> for an MPEG-2 stream. The parse time is a notional time associated with the current position in the stream of bytes supplied to the parser filter. This time is also tied to the origin of the time stamps in that time stamp zero corresponds to parse time zero.

The <a href="/windows/desktop/DirectShow/mpeg-2-splitter">MPEG-2 Splitter</a> filter implements this interface. Use this interface to retrieve or set the current stream parse time or to clear the data buffer of its current data.

## -inheritance

The <b>IAMParse</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMParse</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

