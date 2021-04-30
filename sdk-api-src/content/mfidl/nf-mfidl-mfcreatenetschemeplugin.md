---
UID: NF:mfidl.MFCreateNetSchemePlugin
title: MFCreateNetSchemePlugin function (mfidl.h)
description: Creates the scheme handler for the network source.
helpviewer_keywords: ["MFCreateNetSchemePlugin","MFCreateNetSchemePlugin function [Media Foundation]","f08de332-2b05-4fee-be45-d4928f5f4ef2","mf.mfcreatenetschemeplugin","mfidl/MFCreateNetSchemePlugin"]
old-location: mf\mfcreatenetschemeplugin.htm
tech.root: mf
ms.assetid: f08de332-2b05-4fee-be45-d4928f5f4ef2
ms.date: 12/05/2018
ms.keywords: MFCreateNetSchemePlugin, MFCreateNetSchemePlugin function [Media Foundation], f08de332-2b05-4fee-be45-d4928f5f4ef2, mf.mfcreatenetschemeplugin, mfidl/MFCreateNetSchemePlugin
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
 - MFCreateNetSchemePlugin
 - mfidl/MFCreateNetSchemePlugin
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
 - MFCreateNetSchemePlugin
---

# MFCreateNetSchemePlugin function


## -description

Creates the scheme handler for the network source.

## -parameters

### -param riid [in]

Interface identifier (IID) of the interface to retrieve.

### -param ppvHandler [out]

Receives a pointer to the requested interface. The caller must release the interface. The scheme handler exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler">IMFSchemeHandler</a> interface.

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

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>