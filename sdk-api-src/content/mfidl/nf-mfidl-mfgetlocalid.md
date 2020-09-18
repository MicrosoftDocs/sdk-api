---
UID: NF:mfidl.MFGetLocalId
title: MFGetLocalId function (mfidl.h)
description: Gets the local system ID.
helpviewer_keywords: ["MFGetLocalId","MFGetLocalId function [Media Foundation]","mf.mfgetlocalid","mfidl/MFGetLocalId"]
old-location: mf\mfgetlocalid.htm
tech.root: mf
ms.assetid: 24EA8907-9EBF-42FF-8823-05D48E27F9EA
ms.date: 12/05/2018
ms.keywords: MFGetLocalId, MFGetLocalId function [Media Foundation], mf.mfgetlocalid, mfidl/MFGetLocalId
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetLocalId
 - mfidl/MFGetLocalId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFGetLocalId
---

# MFGetLocalId function


## -description

Gets the local system ID.

## -parameters

### -param verifier [in]

Application-specific verifier value.

### -param size

Length in bytes of verifier.

### -param id [in]

Returned ID string.  This value must be freed by the caller by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>