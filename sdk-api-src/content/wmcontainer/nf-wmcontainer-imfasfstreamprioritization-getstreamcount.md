---
UID: NF:wmcontainer.IMFASFStreamPrioritization.GetStreamCount
title: IMFASFStreamPrioritization::GetStreamCount (wmcontainer.h)
description: Note  This interface is not implemented in this version of Media Foundation. Retrieves the number of entries in the stream priority list.
helpviewer_keywords: ["8c9dacbb-a952-411e-82df-0c8768d0b3fe","GetStreamCount","GetStreamCount method [Media Foundation]","GetStreamCount method [Media Foundation]","IMFASFStreamPrioritization interface","IMFASFStreamPrioritization interface [Media Foundation]","GetStreamCount method","IMFASFStreamPrioritization.GetStreamCount","IMFASFStreamPrioritization::GetStreamCount","mf.imfasfstreamprioritization_getstreamcount","wmcontainer/IMFASFStreamPrioritization::GetStreamCount"]
old-location: mf\imfasfstreamprioritization_getstreamcount.htm
tech.root: mf
ms.assetid: 8c9dacbb-a952-411e-82df-0c8768d0b3fe
ms.date: 12/05/2018
ms.keywords: 8c9dacbb-a952-411e-82df-0c8768d0b3fe, GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFASFStreamPrioritization interface, IMFASFStreamPrioritization interface [Media Foundation],GetStreamCount method, IMFASFStreamPrioritization.GetStreamCount, IMFASFStreamPrioritization::GetStreamCount, mf.imfasfstreamprioritization_getstreamcount, wmcontainer/IMFASFStreamPrioritization::GetStreamCount
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFStreamPrioritization::GetStreamCount
 - wmcontainer/IMFASFStreamPrioritization::GetStreamCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamPrioritization.GetStreamCount
---

# IMFASFStreamPrioritization::GetStreamCount


## -description

<div class="alert"><b>Note</b>  This interface is not implemented in this version of Media Foundation.</div>
<div> </div>
Retrieves the number of entries in the stream priority list.

## -parameters

### -param pdwStreamCount [out]

Receives the number of streams in the stream priority list.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization">IMFASFStreamPrioritization</a>