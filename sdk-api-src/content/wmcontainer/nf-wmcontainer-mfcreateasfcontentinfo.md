---
UID: NF:wmcontainer.MFCreateASFContentInfo
title: MFCreateASFContentInfo function (wmcontainer.h)
description: Creates the ASF Header Object object.
helpviewer_keywords: ["00460f79-7033-4893-88c0-b1c939441f70","MFCreateASFContentInfo","MFCreateASFContentInfo function [Media Foundation]","mf.mfcreateasfcontentinfo","wmcontainer/MFCreateASFContentInfo"]
old-location: mf\mfcreateasfcontentinfo.htm
tech.root: mf
ms.assetid: 00460f79-7033-4893-88c0-b1c939441f70
ms.date: 12/05/2018
ms.keywords: 00460f79-7033-4893-88c0-b1c939441f70, MFCreateASFContentInfo, MFCreateASFContentInfo function [Media Foundation], mf.mfcreateasfcontentinfo, wmcontainer/MFCreateASFContentInfo
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFCreateASFContentInfo
 - wmcontainer/MFCreateASFContentInfo
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
 - MFCreateASFContentInfo
---

# MFCreateASFContentInfo function


## -description

Creates the <a href="/windows/desktop/medfound/asf-file-structure">ASF Header Object</a> object.

## -parameters

### -param ppIContentInfo

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface. The caller must release the interface.

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