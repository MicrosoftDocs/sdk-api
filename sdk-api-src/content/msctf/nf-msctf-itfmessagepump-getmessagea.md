---
UID: NF:msctf.ITfMessagePump.GetMessageA
title: ITfMessagePump::GetMessageA (msctf.h)
description: ITfMessagePump::GetMessageA method
helpviewer_keywords: ["GetMessageA","GetMessageA method [Text Services Framework]","GetMessageA method [Text Services Framework]","ITfMessagePump interface","ITfMessagePump interface [Text Services Framework]","GetMessageA method","ITfMessagePump.GetMessageA","ITfMessagePump::GetMessageA","_tsf_itfmessagepump_getmessagea_ref","msctf/ITfMessagePump::GetMessageA","tsf.itfmessagepump_getmessagea"]
old-location: tsf\itfmessagepump_getmessagea.htm
tech.root: TSF
ms.assetid: a1d66377-fca1-4c9c-ac59-a1417d8ab190
ms.date: 12/05/2018
ms.keywords: GetMessageA, GetMessageA method [Text Services Framework], GetMessageA method [Text Services Framework],ITfMessagePump interface, ITfMessagePump interface [Text Services Framework],GetMessageA method, ITfMessagePump.GetMessageA, ITfMessagePump::GetMessageA, _tsf_itfmessagepump_getmessagea_ref, msctf/ITfMessagePump::GetMessageA, tsf.itfmessagepump_getmessagea
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfMessagePump::GetMessageA
 - msctf/ITfMessagePump::GetMessageA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfMessagePump.GetMessageA
 - getmessagea
---

# ITfMessagePump::GetMessageA


## -description

Obtains a message from the message queue and does not return until a message is obtained. This is the ANSI version of this method.

## -parameters

### -param pMsg [out]

Pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that receives message data.

### -param hwnd [in]

Handle to the window whose messages are obtained. The window must belong to the current thread. If this value is <b>NULL</b>, this method obtains messages for any window that belongs to the calling thread.

### -param wMsgFilterMin [in]

Specifies the lowest message value obtained.

### -param wMsgFilterMax [in]

Specifies the highest message value obtained.

### -param pfResult [out]

Pointer to a BOOL value that receives the return value from the <b>GetMessage</b> function.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

If <i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are both zero, this method returns all available messages; that is, no range filtering is performed.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfmessagepump">ITfMessagePump</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>