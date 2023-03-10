---
UID: NF:imm.ImmEnumInputContext
title: ImmEnumInputContext function (imm.h)
description: The ImmEnumInputContext function (imm.h) retrieves the input context for the specified thread.
helpviewer_keywords: ["0","1","ImmEnumInputContext","ImmEnumInputContext function [Internationalization for Windows Applications]","Thread ID","_win32_ImmEnumInputContext","imm/ImmEnumInputContext","intl.immenuminputcontext"]
old-location: intl\immenuminputcontext.htm
tech.root: Intl
ms.assetid: b066af9a-5bcc-468b-bc1b-79b549a9e55c
ms.date: 08/04/2022
ms.keywords: 0, 1, ImmEnumInputContext, ImmEnumInputContext function [Internationalization for Windows Applications], Thread ID, _win32_ImmEnumInputContext, imm/ImmEnumInputContext, intl.immenuminputcontext
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
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
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmEnumInputContext
 - imm/ImmEnumInputContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
api_name:
 - ImmEnumInputContext
---

# ImmEnumInputContext function


## -description

Retrieves the input context for the specified thread.

## -parameters

### -param idThread [in]

Identifier for the thread. This parameter can have one of the following values.

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
Current thread.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Current process.

</td>
</tr>
<tr>
<td width="40%"><a id="Thread_ID"></a><a id="thread_id"></a><a id="THREAD_ID"></a><dl>
<dt><b>Thread ID</b></dt>
</dl>
</td>
<td width="60%">
Identifier of the thread for which to enumerate the context. This thread identifier can belong to another process.

</td>
</tr>
</table>

### -param lpfn [in]

Pointer to the enumeration callback function. For more information, see <a href="/windows/desktop/api/imm/nc-imm-imcenumproc">EnumInputContext</a>.

### -param lParam [in]

Application-supplied data. The function passes this data to the callback function.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

This function calls the application callback function for each enumerated input context, and passes the specified <i>lParam</i> value.

## -see-also

<a href="/windows/desktop/api/imm/nc-imm-imcenumproc">EnumInputContext</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
