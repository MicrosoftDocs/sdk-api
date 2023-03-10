---
UID: NF:strmif.IDvdControl2.SetGPRM
title: IDvdControl2::SetGPRM (strmif.h)
description: The SetGPRM method sets a general parameter register value.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SetGPRM method","IDvdControl2.SetGPRM","IDvdControl2::SetGPRM","IDvdControl2SetGPRM","SetGPRM","SetGPRM method [DirectShow]","SetGPRM method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_setgprm","strmif/IDvdControl2::SetGPRM"]
old-location: dshow\idvdcontrol2_setgprm.htm
tech.root: dshow
ms.assetid: 192bbf1d-a5de-4acf-b8d6-8a5f733da3a6
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetGPRM method, IDvdControl2.SetGPRM, IDvdControl2::SetGPRM, IDvdControl2SetGPRM, SetGPRM, SetGPRM method [DirectShow], SetGPRM method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setgprm, strmif/IDvdControl2::SetGPRM
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl2::SetGPRM
 - strmif/IDvdControl2::SetGPRM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SetGPRM
---

# IDvdControl2::SetGPRM


## -description

The <code>SetGPRM</code> method sets a general parameter register value.

## -parameters

### -param ulIndex [in]

Register index; may be a value from zero through 15.

### -param wValue [in]

A 16-bit value contained in the specified register.

### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.

### -param ppCmd [out]

Receives a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.

## -returns

Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulIndex</i> parameter is greater than 15 or any other of the input parameters are invalid.

</td>
</tr>
</table>

## -remarks

A DVD disc uses general parameter registers to store various types of information. By manually setting one or more of these registers, an application might be able to provide certain custom functionality. This is an advanced command and should not be used unless you have a thorough understanding of the DVD specification.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>none</td>
<td>All</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getallgprms">IDvdInfo2::GetAllGPRMs</a>