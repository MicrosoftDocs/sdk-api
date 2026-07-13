---
UID: NF:wmsdkidl.WMCreateDRMTranscryptionManager
title: WMCreateDRMTranscryptionManager function (wmsdkidl.h)
description: The WMCreateDRMTranscryptionManager function creates a manager for DRM transcryptor objects.
helpviewer_keywords: ["WMCreateDRMTranscryptionManager","WMCreateDRMTranscryptionManager function [windows Media Format]","wmformat.wmcreatedrmtranscryptionmanager","wmsdkidl/WMCreateDRMTranscryptionManager"]
old-location: wmformat\wmcreatedrmtranscryptionmanager.htm
tech.root: wmformat
ms.assetid: 15bae3af-e601-4865-aee2-a36931c7813d
ms.date: 4/26/2023
ms.keywords: WMCreateDRMTranscryptionManager, WMCreateDRMTranscryptionManager function [windows Media Format], wmformat.wmcreatedrmtranscryptionmanager, wmsdkidl/WMCreateDRMTranscryptionManager
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
 - WMCreateDRMTranscryptionManager
 - wmsdkidl/WMCreateDRMTranscryptionManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMCreateDRMTranscryptionManager
---

# WMCreateDRMTranscryptionManager function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMCreateDRMTranscryptionManager</b> function creates a manager for DRM transcryptor objects.

## -parameters

### -param ppTranscryptionManager

Address of a pointer to the <a href="/previous-versions/windows/desktop/legacy/dd798365(v=vs.85)">IWMDRMTranscryptionManager</a> interface of the newly created DRM transcryptor object manager.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.