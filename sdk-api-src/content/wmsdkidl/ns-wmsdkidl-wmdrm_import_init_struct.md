---
UID: NS:wmsdkidl.WMDRM_IMPORT_INIT_STRUCT
title: WMDRM_IMPORT_INIT_STRUCT (wmsdkidl.h)
description: The WMDRM_IMPORT_INIT_STRUCT structure holds the encrypted session key and content key used in importing protected content.
helpviewer_keywords: ["WMDRM_IMPORT_INIT_STRUCT","WMDRM_IMPORT_INIT_STRUCT structure [windows Media Format]","structure [windows Media Format]","wmformat.wmdrm_import_init_struct","wmsdkidl/WMDRM_IMPORT_INIT_STRUCT"]
old-location: wmformat\wmdrm_import_init_struct.htm
tech.root: wmformat
ms.assetid: 191b844e-5760-44d7-9b27-9fa87fead90f
ms.date: 4/26/2023
ms.keywords: WMDRM_IMPORT_INIT_STRUCT, WMDRM_IMPORT_INIT_STRUCT structure [windows Media Format], structure [windows Media Format], wmformat.wmdrm_import_init_struct, wmsdkidl/WMDRM_IMPORT_INIT_STRUCT
req.header: wmsdkidl.h
req.include-header: Drmexternals.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 11 SDK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMDRM_IMPORT_INIT_STRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMDRM_IMPORT_INIT_STRUCT
 - wmsdkidl/WMDRM_IMPORT_INIT_STRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmsdkidl.h
api_name:
 - WMDRM_IMPORT_INIT_STRUCT
---

# WMDRM_IMPORT_INIT_STRUCT structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMDRM_IMPORT_INIT_STRUCT</b> structure holds the encrypted session key and content key used in importing protected content.

## -struct-fields

### -field dwVersion

Version.

### -field cbEncryptedSessionKeyMessage

Size of the encrypted session key message in bytes.

### -field pbEncryptedSessionKeyMessage

Address of a buffer containing the encrypted session key message. This message is contained in a field of a <a href="/windows/desktop/wmformat/wmdrm-import-session-key">WMDRM_IMPORT_SESSION_KEY</a> structure. The message and its associated key data are both encrypted with the Windows Media DRM machine public key.

### -field cbEncryptedKeyMessage

Size of the encrypted key message in bytes.

### -field pbEncryptedKeyMessage

Address of a buffer containing the encrypted key message. This message is contained in a field of a <a href="/windows/desktop/wmformat/wmdrm-import-content-key">WMDRM_IMPORT_CONTENT_KEY</a> structure. The message and its associated key data are both encrypted with the Windows Media DRM machine public key.

## -remarks

This structure is used to initialize protected stream sample writing in a call to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples">IWMDRMWriter3::SetProtectStreamSamples</a> method.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>