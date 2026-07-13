---
UID: NF:mpeg2psiparser.IPMT.GetPcrPid
title: IPMT::GetPcrPid (mpeg2psiparser.h)
description: The GetPcrPid method returns the packet identifier (PID) of the packets that contain the Program Clock Reference (PCR) fields for this program.
helpviewer_keywords: ["GetPcrPid","GetPcrPid method [Microsoft TV Technologies]","GetPcrPid method [Microsoft TV Technologies]","IPMT interface","IPMT interface [Microsoft TV Technologies]","GetPcrPid method","IPMT.GetPcrPid","IPMT::GetPcrPid","IPMTGetPcrPid","mpeg2psiparser/IPMT::GetPcrPid","mstv.ipmt_getpcrpid"]
old-location: mstv\ipmt_getpcrpid.htm
tech.root: mstv
ms.assetid: 0099e5b3-d573-47b9-9581-fbb9fee3ca16
ms.date: 12/05/2018
ms.keywords: GetPcrPid, GetPcrPid method [Microsoft TV Technologies], GetPcrPid method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetPcrPid method, IPMT.GetPcrPid, IPMT::GetPcrPid, IPMTGetPcrPid, mpeg2psiparser/IPMT::GetPcrPid, mstv.ipmt_getpcrpid
req.header: mpeg2psiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IPMT::GetPcrPid
 - mpeg2psiparser/IPMT::GetPcrPid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetPcrPid
---

# IPMT::GetPcrPid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPcrPid</b> method returns the packet identifier (PID) of the packets that contain the Program Clock Reference (PCR) fields for this program.

## -parameters

### -param pPidVal [out]

Receives the PCR_PID field.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>