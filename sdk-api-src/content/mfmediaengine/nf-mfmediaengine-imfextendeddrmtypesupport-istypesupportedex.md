---
UID: NF:mfmediaengine.IMFExtendedDRMTypeSupport.IsTypeSupportedEx
tech.root: mf
title: IMFExtendedDRMTypeSupport::IsTypeSupportedEx
ms.date: 04/06/2022
targetos: Windows
description: Queries wether the specified content type is supported for the specified key system.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfmediaengine.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFExtendedDRMTypeSupport::IsTypeSupportedEx
f1_keywords:
 - IMFExtendedDRMTypeSupport::IsTypeSupportedEx
 - mfmediaengine/IMFExtendedDRMTypeSupport::IsTypeSupportedEx
dev_langs:
 - c++
helpviewer_keywords:
 - IsTypeSupportedEx
---

## -description

Queries whether the specified content type is supported for the specified key system.

## -parameters

### -param type [in]

A **BSTR** identifying the features for which support is queried queried. This parameter accepts RFC 2045 Content-Type strings to specify media type and subtype identifiers, and RFC 6381 Codecs identifiers for the codecs required. These base strings are consistent with those used in the HTML5 HTMLMediaElement canPlayType method. RFC 2045 allows for additional, custom parameters as modifiers in the form of ";&lt;parameter&gt;=&lt;name&gt;\[=&lt;value&gt;\] \[,&lt;name&gt;\[=&lt;value&gt;\]". RFC 2045 compliant parsers must ignore these parameters if not recognized. For the feature queries, <parameter> is named feature.

The implementation requires the RFC 2045 media type and subtype identifiers, for example "video/mp4", and RFC 6381 codec parameter codec=”&lt;video codec&gt;\[,&lt;audio codec&gt;\]” to always be present in order to provide valid query results.

Note that the terms content type and type are well known historically as MIME type.

### -param keySystem [in]

A **BSTR** identifying the PlayReady namespace to check query against, specifying hardware or software protection. Use "com.microsoft.playready.recommendation.3000" for hardware queries (PlayReady must have support for hardware offload), "com.microsoft.playready.recommendation.2000" for explicitly querying for software protection support, and "com.microsoft.playready.recommendation" for general queries (must answer for software protection support to guarantee backward compatibility).

### -param pAnswer [out]

A value from the [MF_MEDIA_ENGINE_CANPLAY](ne-mfmediaengine-mf_media_engine_canplay) enumeration indicating if the queried capabilities are likely supported, are possibly supported, or are unsupported.



## -returns

S_OK on success.

## -remarks

## -see-also

