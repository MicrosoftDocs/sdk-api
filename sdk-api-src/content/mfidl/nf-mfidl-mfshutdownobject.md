---
UID: NF:mfidl.MFShutdownObject
title: MFShutdownObject function (mfidl.h)
description: Shuts down a Media Foundation object and releases all resources associated with the object. (MFShutdownObject)
helpviewer_keywords: ["MFShutdownObject","MFShutdownObject function [Media Foundation]","a7dc3d4a-f21e-4af8-bee0-2d5f2cf28587","mf.mfshutdownobject","mfidl/MFShutdownObject"]
old-location: mf\mfshutdownobject.htm
tech.root: mf
ms.assetid: a7dc3d4a-f21e-4af8-bee0-2d5f2cf28587
ms.date: 12/05/2018
ms.keywords: MFShutdownObject, MFShutdownObject function [Media Foundation], a7dc3d4a-f21e-4af8-bee0-2d5f2cf28587, mf.mfshutdownobject, mfidl/MFShutdownObject
req.header: mfidl.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFShutdownObject
 - mfidl/MFShutdownObject
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
 - MFShutdownObject
---

# MFShutdownObject function


## -description

Shuts down a Media Foundation object and releases all resources associated with the object.

This function is a helper function that wraps the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">IMFShutdown::Shutdown</a> method. The function queries the object for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a> interface and, if successful, calls <b>Shutdown</b> on the object.

## -parameters

### -param pUnk

Pointer to the <b>IUnknown</b> interface of the object.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
</table>

## -remarks

This function is not related to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function, which shuts down the Media Foundation platform, as described in <a href="/windows/desktop/medfound/initializing-media-foundation">Initializing Media Foundation</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
