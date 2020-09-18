---
UID: NF:mfidl.MFCreateStandardQualityManager
title: MFCreateStandardQualityManager function (mfidl.h)
description: Creates the default implementation of the quality manager.
helpviewer_keywords: ["9abaa474-8a00-4e36-897d-9de9578333b7","MFCreateStandardQualityManager","MFCreateStandardQualityManager function [Media Foundation]","mf.mfcreatestandardqualitymanager","mfidl/MFCreateStandardQualityManager"]
old-location: mf\mfcreatestandardqualitymanager.htm
tech.root: mf
ms.assetid: 9abaa474-8a00-4e36-897d-9de9578333b7
ms.date: 12/05/2018
ms.keywords: 9abaa474-8a00-4e36-897d-9de9578333b7, MFCreateStandardQualityManager, MFCreateStandardQualityManager function [Media Foundation], mf.mfcreatestandardqualitymanager, mfidl/MFCreateStandardQualityManager
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
 - MFCreateStandardQualityManager
 - mfidl/MFCreateStandardQualityManager
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
 - MFCreateStandardQualityManager
---

# MFCreateStandardQualityManager function


## -description

Creates the default implementation of the quality manager.

## -parameters

### -param ppQualityManager [out]

Receives a pointer to the quality manager's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a> interface. The caller must release the interface.

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
The method succeeded.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>