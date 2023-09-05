---
UID: NF:bdaiface.IBDA_DiseqCommand.put_DiseqLNBSource
title: IBDA_DiseqCommand::put_DiseqLNBSource (bdaiface.h)
description: Sets the low-noise block (LNB) converter source.
helpviewer_keywords: ["0","1","2","3","IBDA_DiseqCommand interface [Microsoft TV Technologies]","put_DiseqLNBSource method","IBDA_DiseqCommand.put_DiseqLNBSource","IBDA_DiseqCommand::put_DiseqLNBSource","bdaiface/IBDA_DiseqCommand::put_DiseqLNBSource","mstv.ibda_diseqcommand_put_diseqlnbsource","put_DiseqLNBSource","put_DiseqLNBSource method [Microsoft TV Technologies]","put_DiseqLNBSource method [Microsoft TV Technologies]","IBDA_DiseqCommand interface"]
old-location: mstv\ibda_diseqcommand_put_diseqlnbsource.htm
tech.root: mstv
ms.assetid: 09ed3d1d-026a-43b3-863b-a77260e082d8
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, IBDA_DiseqCommand interface [Microsoft TV Technologies],put_DiseqLNBSource method, IBDA_DiseqCommand.put_DiseqLNBSource, IBDA_DiseqCommand::put_DiseqLNBSource, bdaiface/IBDA_DiseqCommand::put_DiseqLNBSource, mstv.ibda_diseqcommand_put_diseqlnbsource, put_DiseqLNBSource, put_DiseqLNBSource method [Microsoft TV Technologies], put_DiseqLNBSource method [Microsoft TV Technologies],IBDA_DiseqCommand interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_DiseqCommand::put_DiseqLNBSource
 - bdaiface/IBDA_DiseqCommand::put_DiseqLNBSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DiseqCommand.put_DiseqLNBSource
---

# IBDA_DiseqCommand::put_DiseqLNBSource


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sets the low-noise block (LNB) converter source.

## -parameters

### -param ulLNBSource [in]

The LNB converter source to use.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Source position A.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Source position B.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Source position C.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Source position D.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_diseqcommand">IBDA_DiseqCommand</a>