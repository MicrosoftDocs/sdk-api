---
UID: NE:textstor.__MIDL___MIDL_itf_textstor_0000_0000_0002
title: TsLayoutCode (textstor.h)
description: Elements of the TsLayoutCode enumeration are used to specify the type of layout change in an ITextStoreACPSink::OnLayoutChange or ITextStoreAnchorSink::OnLayoutChange notification.
helpviewer_keywords: ["TS_LC_CHANGE","TS_LC_CREATE","TS_LC_DESTROY","TsLayoutCode","TsLayoutCode enumeration [Text Services Framework]","_tsf_tslayoutcode_ref","textstor/TS_LC_CHANGE","textstor/TS_LC_CREATE","textstor/TS_LC_DESTROY","textstor/TsLayoutCode","tsf.tslayoutcode"]
old-location: tsf\tslayoutcode.htm
tech.root: TSF
ms.assetid: 879f83ba-211b-49f6-93b2-6cde5f50fc24
ms.date: 12/05/2018
ms.keywords: TS_LC_CHANGE, TS_LC_CREATE, TS_LC_DESTROY, TsLayoutCode, TsLayoutCode enumeration [Text Services Framework], _tsf_tslayoutcode_ref, textstor/TS_LC_CHANGE, textstor/TS_LC_CREATE, textstor/TS_LC_DESTROY, textstor/TsLayoutCode, tsf.tslayoutcode
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TsLayoutCode
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_textstor_0000_0000_0002
 - textstor/__MIDL___MIDL_itf_textstor_0000_0000_0002
 - TsLayoutCode
 - textstor/TsLayoutCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TsLayoutCode
---

# TsLayoutCode enumeration


## -description

Elements of the <b>TsLayoutCode</b> enumeration are used to specify the type of layout change in an <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlayoutchange">ITextStoreACPSink::OnLayoutChange</a> or <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onlayoutchange">ITextStoreAnchorSink::OnLayoutChange</a> notification.

## -enum-fields

### -field TS_LC_CREATE:0

The view has just been created.

### -field TS_LC_CHANGE:1

The view layout has changed.

### -field TS_LC_DESTROY:2

The view is about to be destroyed.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlayoutchange">ITextStoreACPSink::OnLayoutChange
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onlayoutchange">ITextStoreAnchorSink::OnLayoutChange
      </a>
