---
UID: NF:textstor.IAnchor.GetChangeHistory
title: IAnchor::GetChangeHistory (textstor.h)
description: The IAnchor::GetChangeHistory method gets the history of deletions that have occurred immediately preceding or following the anchor.
helpviewer_keywords: ["GetChangeHistory","GetChangeHistory method [Text Services Framework]","GetChangeHistory method [Text Services Framework]","IAnchor interface","IAnchor interface [Text Services Framework]","GetChangeHistory method","IAnchor.GetChangeHistory","IAnchor::GetChangeHistory","TS_CH_FOLLOWING_DEL","TS_CH_PRECEDING_DEL","textstor/IAnchor::GetChangeHistory","tsf.ianchor_getchangehistory"]
old-location: tsf\ianchor_getchangehistory.htm
tech.root: TSF
ms.assetid: d373a379-1d27-4438-abaf-2e11f2332790
ms.date: 12/05/2018
ms.keywords: GetChangeHistory, GetChangeHistory method [Text Services Framework], GetChangeHistory method [Text Services Framework],IAnchor interface, IAnchor interface [Text Services Framework],GetChangeHistory method, IAnchor.GetChangeHistory, IAnchor::GetChangeHistory, TS_CH_FOLLOWING_DEL, TS_CH_PRECEDING_DEL, textstor/IAnchor::GetChangeHistory, tsf.ianchor_getchangehistory
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - IAnchor::GetChangeHistory
 - textstor/IAnchor::GetChangeHistory
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
 - IAnchor.GetChangeHistory
---

# IAnchor::GetChangeHistory


## -description

The <b>IAnchor::GetChangeHistory</b> method gets the history of deletions that have occurred immediately preceding or following the anchor.

## -parameters

### -param pdwHistory [out]

Bit field flags that specify that deletions have occurred immediately preceding or following the anchor. One or both of the following values can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_CH_PRECEDING_DEL"></a><a id="ts_ch_preceding_del"></a><dl>
<dt><b>TS_CH_PRECEDING_DEL</b></dt>
</dl>
</td>
<td width="60%">
Text preceding the anchor has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_CH_FOLLOWING_DEL"></a><a id="ts_ch_following_del"></a><dl>
<dt><b>TS_CH_FOLLOWING_DEL</b></dt>
</dl>
</td>
<td width="60%">
Text following the anchor has been deleted.

</td>
</tr>
</table>

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
The value of <i>pdwHistory</i> is invalid.

</td>
</tr>
</table>

## -remarks

The <i>pdwHistory</i> change flags must be set when deletions adjacent to the anchor have occurred.

The change flags remain set until they are cleared with a call to <a href="/windows/desktop/api/textstor/nf-textstor-ianchor-clearchangehistory">IAnchor::ClearChangeHistory</a>.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-clearchangehistory">IAnchor::ClearChangeHistory
      </a>