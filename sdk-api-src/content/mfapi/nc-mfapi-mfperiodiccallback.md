---
UID: NC:mfapi.MFPERIODICCALLBACK
title: MFPERIODICCALLBACK (mfapi.h)
description: Callback function for the MFAddPeriodicCallback function.
helpviewer_keywords: ["9449fa04-867c-4f27-a05c-ff0d6e912c53","MFPERIODICCALLBACK","MFPERIODICCALLBACK callback","MFPERIODICCALLBACK callback function [Media Foundation]","mf.mfperiodiccallback_callback","mfapi/MFPERIODICCALLBACK"]
old-location: mf\mfperiodiccallback_callback.htm
tech.root: mf
ms.assetid: 9449fa04-867c-4f27-a05c-ff0d6e912c53
ms.date: 12/05/2018
ms.keywords: 9449fa04-867c-4f27-a05c-ff0d6e912c53, MFPERIODICCALLBACK, MFPERIODICCALLBACK callback, MFPERIODICCALLBACK callback function [Media Foundation], mf.mfperiodiccallback_callback, mfapi/MFPERIODICCALLBACK
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFPERIODICCALLBACK
 - mfapi/MFPERIODICCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - mfapi.h
api_name:
 - MFPERIODICCALLBACK
---

# MFPERIODICCALLBACK callback function


## -description

Callback function for the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback">MFAddPeriodicCallback</a> function.

## -parameters

### -param pContext [in]

Pointer to the <b>IUnknown</b> interface, or <b>NULL</b>. This pointer is specified by the caller in the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback">MFAddPeriodicCallback</a> function.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
