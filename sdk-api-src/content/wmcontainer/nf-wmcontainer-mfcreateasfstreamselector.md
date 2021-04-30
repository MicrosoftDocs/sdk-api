---
UID: NF:wmcontainer.MFCreateASFStreamSelector
title: MFCreateASFStreamSelector function (wmcontainer.h)
description: Creates the ASF stream selector.
helpviewer_keywords: ["71b1af5b-f127-463f-9720-72e789bb2cd1","MFCreateASFStreamSelector","MFCreateASFStreamSelector function [Media Foundation]","mf.mfcreateasfstreamselector","wmcontainer/MFCreateASFStreamSelector"]
old-location: mf\mfcreateasfstreamselector.htm
tech.root: mf
ms.assetid: 71b1af5b-f127-463f-9720-72e789bb2cd1
ms.date: 12/05/2018
ms.keywords: 71b1af5b-f127-463f-9720-72e789bb2cd1, MFCreateASFStreamSelector, MFCreateASFStreamSelector function [Media Foundation], mf.mfcreateasfstreamselector, wmcontainer/MFCreateASFStreamSelector
req.header: wmcontainer.h
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
 - MFCreateASFStreamSelector
 - wmcontainer/MFCreateASFStreamSelector
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
 - MFCreateASFStreamSelector
---

# MFCreateASFStreamSelector function


## -description

Creates the ASF stream selector.

## -parameters

### -param pIASFProfile

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a> interface.

### -param ppSelector

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a> interface. The caller must release the interface.

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

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>