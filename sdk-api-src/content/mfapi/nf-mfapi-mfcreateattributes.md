---
UID: NF:mfapi.MFCreateAttributes
title: MFCreateAttributes function (mfapi.h)
description: Creates an empty attribute store.
helpviewer_keywords: ["MFCreateAttributes","MFCreateAttributes function [Media Foundation]","a79b1edd-5ca1-4550-a6ce-58073155affd","mf.mfcreateattributes","mfapi/MFCreateAttributes"]
old-location: mf\mfcreateattributes.htm
tech.root: mf
ms.assetid: a79b1edd-5ca1-4550-a6ce-58073155affd
ms.date: 12/05/2018
ms.keywords: MFCreateAttributes, MFCreateAttributes function [Media Foundation], a79b1edd-5ca1-4550-a6ce-58073155affd, mf.mfcreateattributes, mfapi/MFCreateAttributes
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateAttributes
 - mfapi/MFCreateAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateAttributes
---

# MFCreateAttributes function


## -description

Creates an empty attribute store.

## -parameters

### -param ppMFAttributes [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. The caller must release the interface.

### -param cInitialSize [in]

The initial number of elements allocated for the attribute store. The attribute store grows as needed.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes. For more information, see <a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>.

For a complete list of all the defined attribute GUIDs in Media Foundation, see <a href="/windows/desktop/medfound/media-foundation-attributes">Media Foundation Attributes</a>.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes in Media Foundation</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>