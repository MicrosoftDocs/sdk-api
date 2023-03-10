---
UID: NN:tapi3ds.ITAMMediaFormat
title: ITAMMediaFormat (tapi3ds.h)
description: The ITAMMediaFormat interface (tapi3ds.h) sets and gets DirectShow media format.
helpviewer_keywords: ["ITAMMediaFormat","ITAMMediaFormat interface [TAPI 2.2]","ITAMMediaFormat interface [TAPI 2.2]","described","_tapi3_itammediaformat","tapi3.itammediaformat","tapi3ds/ITAMMediaFormat"]
old-location: tapi3\itammediaformat.htm
tech.root: tapi3
ms.assetid: 82728afe-5743-4b45-86e6-32df021a2a5f
ms.date: 08/10/2022
ms.keywords: ITAMMediaFormat, ITAMMediaFormat interface [TAPI 2.2], ITAMMediaFormat interface [TAPI 2.2],described, _tapi3_itammediaformat, tapi3.itammediaformat, tapi3ds/ITAMMediaFormat
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAMMediaFormat
 - tapi3ds/ITAMMediaFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAMMediaFormat
---

# ITAMMediaFormat interface


## -description

The 
<b>ITAMMediaFormat</b> interface sets and gets DirectShow media format. The format is described using the 
<b>AM_MEDIA_TYPE</b> structure. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. This interface is exposed on a 
<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a> only if an MSP is involved in terminal creation and implements this interface. The 
<b>ITAMMediaFormat</b> interface is created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.

On addresses where a variety of formats are supported (such as Wave MSP addresses, which are used on most modems and voice boards), this media format must be set or the terminal will not be able to connect.

For other addresses, such as those implemented over IP, the format may be fixed/predetermined. In that case, a call to set format will fail if the format is not the same as the predetermined format.

## -inheritance

The <b>ITAMMediaFormat</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITAMMediaFormat</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
