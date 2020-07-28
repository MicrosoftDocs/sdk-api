---
UID: NF:mfidl.MFCreateSequencerSource
title: MFCreateSequencerSource function (mfidl.h)
description: Creates the sequencer source.
helpviewer_keywords: ["MFCreateSequencerSource","MFCreateSequencerSource function [Media Foundation]","e4640731-f262-4ceb-8d17-908c2c6b192e","mf.mfcreatesequencersource","mfidl/MFCreateSequencerSource"]
old-location: mf\mfcreatesequencersource.htm
tech.root: mf
ms.assetid: e4640731-f262-4ceb-8d17-908c2c6b192e
ms.date: 12/05/2018
ms.keywords: MFCreateSequencerSource, MFCreateSequencerSource function [Media Foundation], e4640731-f262-4ceb-8d17-908c2c6b192e, mf.mfcreatesequencersource, mfidl/MFCreateSequencerSource
f1_keywords:
- mfidl/MFCreateSequencerSource
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mf.dll
api_name:
- MFCreateSequencerSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateSequencerSource function


## -description



Creates the sequencer source.




## -parameters




### -param pReserved

Reserved. Must be <b>NULL</b>.


### -param ppSequencerSource

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource">IMFSequencerSource</a> interface of the sequencer source. The caller must release the interface.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sequencer-source">Sequencer Source</a>
 

 

