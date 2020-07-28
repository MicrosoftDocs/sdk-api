---
UID: NF:wmsdkidl.WMCreateDRMTranscryptionManager
title: WMCreateDRMTranscryptionManager function (wmsdkidl.h)
description: The WMCreateDRMTranscryptionManager function creates a manager for DRM transcryptor objects.
helpviewer_keywords: ["WMCreateDRMTranscryptionManager","WMCreateDRMTranscryptionManager function [windows Media Format]","wmformat.wmcreatedrmtranscryptionmanager","wmsdkidl/WMCreateDRMTranscryptionManager"]
old-location: wmformat\wmcreatedrmtranscryptionmanager.htm
tech.root: wmformat
ms.assetid: 15bae3af-e601-4865-aee2-a36931c7813d
ms.date: 12/05/2018
ms.keywords: WMCreateDRMTranscryptionManager, WMCreateDRMTranscryptionManager function [windows Media Format], wmformat.wmcreatedrmtranscryptionmanager, wmsdkidl/WMCreateDRMTranscryptionManager
f1_keywords:
- wmsdkidl/WMCreateDRMTranscryptionManager
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wmsdkidl.h
api_name:
- WMCreateDRMTranscryptionManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateDRMTranscryptionManager function


## -description


The <b>WMCreateDRMTranscryptionManager</b> function creates a manager for DRM transcryptor objects.


## -parameters




### -param ppTranscryptionManager

Address of a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd798365(v=vs.85)">IWMDRMTranscryptionManager</a> interface of the newly created DRM transcryptor object manager.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



