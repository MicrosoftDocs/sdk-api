---
UID: NF:mfapi.MFGetPluginControl
title: MFGetPluginControl function (mfapi.h)
description: Gets a pointer to the Microsoft Media Foundation plug-in manager.
helpviewer_keywords: ["MFGetPluginControl","MFGetPluginControl function [Media Foundation]","mf.mfgetplugincontrol","mfapi/MFGetPluginControl"]
old-location: mf\mfgetplugincontrol.htm
tech.root: mf
ms.assetid: 68b25c68-806d-46c3-98f8-8f29d7c21471
ms.date: 12/05/2018
ms.keywords: MFGetPluginControl, MFGetPluginControl function [Media Foundation], mf.mfgetplugincontrol, mfapi/MFGetPluginControl
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - MFGetPluginControl
 - mfapi/MFGetPluginControl
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
 - MFGetPluginControl
---

# MFGetPluginControl function


## -description

Gets a pointer to the Microsoft Media Foundation plug-in manager.

## -parameters

### -param ppPluginControl [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>