---
UID: NF:mfidl.IMFNetCrossOriginSupport.GetSourceOrigin
title: IMFNetCrossOriginSupport::GetSourceOrigin (mfidl.h)
description: Returns the W3C origin of the HTML5 media element.
helpviewer_keywords: ["GetSourceOrigin","GetSourceOrigin method [Media Foundation]","GetSourceOrigin method [Media Foundation]","IMFNetCrossOriginSupport interface","IMFNetCrossOriginSupport interface [Media Foundation]","GetSourceOrigin method","IMFNetCrossOriginSupport.GetSourceOrigin","IMFNetCrossOriginSupport::GetSourceOrigin","mf.imfnetcrossoriginsupport_getsourceorigin","mfidl/IMFNetCrossOriginSupport::GetSourceOrigin"]
old-location: mf\imfnetcrossoriginsupport_getsourceorigin.htm
tech.root: mf
ms.assetid: 84379D86-DB03-4631-9A35-EFE9811B0D33
ms.date: 12/05/2018
ms.keywords: GetSourceOrigin, GetSourceOrigin method [Media Foundation], GetSourceOrigin method [Media Foundation],IMFNetCrossOriginSupport interface, IMFNetCrossOriginSupport interface [Media Foundation],GetSourceOrigin method, IMFNetCrossOriginSupport.GetSourceOrigin, IMFNetCrossOriginSupport::GetSourceOrigin, mf.imfnetcrossoriginsupport_getsourceorigin, mfidl/IMFNetCrossOriginSupport::GetSourceOrigin
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetCrossOriginSupport::GetSourceOrigin
 - mfidl/IMFNetCrossOriginSupport::GetSourceOrigin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCrossOriginSupport.GetSourceOrigin
---

# IMFNetCrossOriginSupport::GetSourceOrigin


## -description



Returns the W3C origin of the HTML5 media element.

## -parameters

### -param wszSourceOrigin [out]

The W3C origin of the HTML5 media element.

## -returns

Returns S_OK upon successful completion.

## -remarks

Use <b>CoTaskMemFree</b> to free the string.

## -see-also

<a href="../mfidl/nn-mfidl-imfnetcrossoriginsupport.md">IMFNetCrossOriginSupport</a>

