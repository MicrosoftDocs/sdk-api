---
UID: NF:wmsecure.WMCreateSecureChannel_Certified
title: WMCreateSecureChannel_Certified function (wmsecure.h)
description: Creates an object that implements IWMSecureChannel.
helpviewer_keywords: ["WMCreateSecureChannel_Certified","WMCreateSecureChannel_Certified function [windows Media Format]","wmformat.wmcreatesecurechannel_certified","wmsecure/WMCreateSecureChannel_Certified"]
old-location: wmformat\wmcreatesecurechannel_certified.htm
tech.root: wmformat
ms.assetid: 0381c653-05e1-417c-beee-40c4aa4271f4
ms.date: 4/26/2023
ms.keywords: WMCreateSecureChannel_Certified, WMCreateSecureChannel_Certified function [windows Media Format], wmformat.wmcreatesecurechannel_certified, wmsecure/WMCreateSecureChannel_Certified
req.header: wmsecure.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMCreateSecureChannel_Certified
 - wmsecure/WMCreateSecureChannel_Certified
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsecure.h
api_name:
 - WMCreateSecureChannel_Certified
---

# WMCreateSecureChannel_Certified function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Creates an object that implements <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>.

## -parameters

### -param ppChannel

Address of a pointer to the <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface of the newly created secure channel object.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>