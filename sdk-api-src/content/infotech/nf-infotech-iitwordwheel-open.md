---
UID: NF:infotech.IITWordWheel.Open
title: IITWordWheel::Open (infotech.h)
description: Opens a word wheel.
helpviewer_keywords: ["IITWordWheel interface [HTML Help Workshop]","Open method","IITWordWheel.Open","IITWordWheel::Open","ITWW_OPEN_CONNECT","Open","Open method [HTML Help Workshop]","Open method [HTML Help Workshop]","IITWordWheel interface","htmlhelp.iitwordwheel_open","infotech/IITWordWheel::Open","refIITWordWheelOpen"]
old-location: htmlhelp\iitwordwheel_open.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheelopen.htm
ms.date: 12/05/2018
ms.keywords: IITWordWheel interface [HTML Help Workshop],Open method, IITWordWheel.Open, IITWordWheel::Open, ITWW_OPEN_CONNECT, Open, Open method [HTML Help Workshop], Open method [HTML Help Workshop],IITWordWheel interface, htmlhelp.iitwordwheel_open, infotech/IITWordWheel::Open, refIITWordWheelOpen
req.header: infotech.h
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
 - IITWordWheel::Open
 - infotech/IITWordWheel::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITWordWheel.Open
---

# IITWordWheel::Open


## -description

Opens a word wheel.

## -parameters

### -param lpITDB [in]

Pointer to <a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitdatabase">database object</a>.

### -param lpszMoniker [in]

Name of word wheel.

### -param dwFlags [in]

One or more of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ITWW_OPEN_CONNECT"></a><a id="itww_open_connect"></a><dl>
<dt><b>ITWW_OPEN_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  If the word wheel resides on a remote computer, connect to the computer during this call to retrieve initialization data. Otherwise the connection is delayed until the first API call that requires this data.</div>
<div> </div>
</td>
</tr>
</table>

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
The word wheel was successfully opened.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ALREADYOPEN</b></dt>
</dl>
</td>
<td width="60%">
Word wheel is already open.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitdatabase">IITDatabase</a>* interface or <i>lpszMoniker</i> parameter was NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E*</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface errors that can occur as storage is opened.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitwordwheel">IITWordWheel</a>