---
UID: NF:bdaiface.IBDA_DiseqCommand.get_DiseqResponse
title: IBDA_DiseqCommand::get_DiseqResponse (bdaiface.h)
description: Gets the driver's response to a Digital Satellite Equipment Control (DiSEqC) command.
helpviewer_keywords: ["IBDA_DiseqCommand interface [Microsoft TV Technologies]","get_DiseqResponse method","IBDA_DiseqCommand.get_DiseqResponse","IBDA_DiseqCommand::get_DiseqResponse","bdaiface/IBDA_DiseqCommand::get_DiseqResponse","get_DiseqResponse","get_DiseqResponse method [Microsoft TV Technologies]","get_DiseqResponse method [Microsoft TV Technologies]","IBDA_DiseqCommand interface","mstv.ibda_diseqcommand_get_diseqresponse"]
old-location: mstv\ibda_diseqcommand_get_diseqresponse.htm
tech.root: mstv
ms.assetid: ed481bfb-dd80-44fa-bf64-a0f8e903ae35
ms.date: 12/05/2018
ms.keywords: IBDA_DiseqCommand interface [Microsoft TV Technologies],get_DiseqResponse method, IBDA_DiseqCommand.get_DiseqResponse, IBDA_DiseqCommand::get_DiseqResponse, bdaiface/IBDA_DiseqCommand::get_DiseqResponse, get_DiseqResponse, get_DiseqResponse method [Microsoft TV Technologies], get_DiseqResponse method [Microsoft TV Technologies],IBDA_DiseqCommand interface, mstv.ibda_diseqcommand_get_diseqresponse
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
 - IBDA_DiseqCommand::get_DiseqResponse
 - bdaiface/IBDA_DiseqCommand::get_DiseqResponse
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
 - IBDA_DiseqCommand.get_DiseqResponse
---

# IBDA_DiseqCommand::get_DiseqResponse


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the driver's response to a Digital Satellite Equipment Control (DiSEqC) command.

## -parameters

### -param ulRequestId [in]

The identifier of the command. The application assigns this value when it calls <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_diseqcommand-put_diseqsendcommand">IBDA_DiseqCommand::put_DiseqSendCommand</a>.

### -param pulcbResponseLen [in, out]

On input, specifies the size of the <i>pbResponse</i> array, in bytes. On output, receives the number of bytes of data written into the <i>pbResponse</i> buffer.

### -param pbResponse [in, out]

Pointer to a byte array that receives the driver's response.

## -returns

This method can return one of these values.

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
<tr>
<td width="40%">
<dl>
<dt><b>BDA_E_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer given in the <i>pbResponse</i> parameter is too small.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_diseqcommand">IBDA_DiseqCommand</a>