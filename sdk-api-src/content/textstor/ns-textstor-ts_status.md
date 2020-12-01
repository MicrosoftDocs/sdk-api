---
UID: NS:textstor.TS_STATUS
title: TS_STATUS (textstor.h)
description: The TS_STATUS structure contains document status data.
helpviewer_keywords: ["TS_STATUS","TS_STATUS structure [Text Services Framework]","_tsf_ts_status_ref","textstor/TS_STATUS","tsf.ts_status"]
old-location: tsf\ts_status.htm
tech.root: TSF
ms.assetid: d27d81f2-8599-4b65-866b-4e8fd2f589f5
ms.date: 12/05/2018
ms.keywords: TS_STATUS, TS_STATUS structure [Text Services Framework], _tsf_ts_status_ref, textstor/TS_STATUS, tsf.ts_status
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TS_STATUS
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_STATUS
 - textstor/TS_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TS_STATUS
---

# TS_STATUS structure


## -description

The <b>TS_STATUS</b> structure contains document status data.

## -struct-fields

### -field dwDynamicFlags

Contains a set of flags that can be changed by an app at run time. For example, an app can enable a check box for the user to reset the document status. This member can contain zero, or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TS_SD_LOADING</td>
<td>The document is loading.</td>
</tr>
<tr>
<td>TS_SD_READONLY</td>
<td>The document is read-only.</td>
</tr>
</table>

### -field dwStaticFlags

Contains a set of flags that cannot be changed at run time. This member can contain zero, or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TS_SS_DISJOINTSEL</td>
<td>The document supports multiple selections.</td>
</tr>
<tr>
<td>TS_SS_REGIONS</td>
<td>The document can contain multiple regions.</td>
</tr>
<tr>
<td>TS_SS_TRANSITORY</td>
<td>The document is expected to have a short usage cycle.</td>
</tr>
<tr>
<td>TS_SS_NOHIDDENTEXT</td>
<td>The document will never contain hidden text.</td>
</tr>
<tr>
<td>TS_SS_TKBAUTOCORRECTENABLE</td>
<td><b>Starting with Windows 8:</b> The document supports autocorrection provided by the touch keyboard.</td>
</tr>
<tr>
<td>TS_SS_TKBPREDICTIONENABLE</td>
<td><b>Starting with Windows 8:</b> The document supports text suggestions provided by the touch keyboard.</td>
</tr>
</table>

## -remarks

The <a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS</a> structure contains document status data.


<a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS</a> is an alias for <b>TS_STATUS</b>.

<b>dwDynamicFlags</b> contains a set of flags that can be changed by an app at run time. For example, an app can enable a check box for the user to reset the status of documentation. This member can contain zero, or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_SD_LOADING</td>
<td>The document is loading.</td>
</tr>
<tr>
<td>TF_SD_READONLY</td>
<td>The document is read-only.</td>
</tr>
<tr>
<td>TS_SD_UIINTEGRATIONENABLE</td>
<td>
<b>Starting with Windows 8.1:</b> The text control owning the document sets this flag to indicate its support of Input Method Editor (IME) UI integration. When specified, the IME should attempt to align the candidate window below the text box instead of floating near the cursor.<div class="alert"><b>Note</b>  Not all IMEs respond to this flag. IME candidate lists are positioned on the screen with sufficient size to allow basic text input. In some cases, the IME may enforce a reasonable minimum size.  An IME might also choose to adjust the candidate window and keyboard input behavior to provide a better user experience, such as using a horizontal candidate list and allowing some keys such as up arrow and down arrow to be sent to the app for scenarios such as suggestion list navigation.</div>
<div> </div>
</td>
</tr>
<tr>
<td>TF_SD_TKBAUTOCORRECTENABLE</td>
<td><b>Starting with Windows 8.1:</b> The document supports autocorrection provided by the touch keyboard. This support can change during the lifetime of the control.</td>
</tr>
<tr>
<td>TF_SD_TKBPREDICTIONENABLE</td>
<td><b>Starting with Windows 8.1:</b> The document supports text suggestions provided by the touch keyboard. This support can change during the lifetime of the control.</td>
</tr>
</table>
 

<b>dwStaticFlags</b> contains a set of flags that cannot be changed at run time. This member can contain zero, or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_SS_DISJOINTSEL</td>
<td>The document supports multiple selections.</td>
</tr>
<tr>
<td>TF_SS_REGIONS</td>
<td>The document can contain multiple regions.</td>
</tr>
<tr>
<td>TF_SS_TRANSITORY</td>
<td>The document is expected to have a short usage cycle.</td>
</tr>
<tr>
<td>TF_SS_TKBAUTOCORRECTENABLE</td>
<td><b>Starting with Windows 8:</b> The document supports autocorrection provided by the touch keyboard.</td>
</tr>
<tr>
<td>TF_SS_TKBPREDICTIONENABLE</td>
<td><b>Starting with Windows 8:</b> The document supports text suggestions provided by the touch keyboard.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getstatus">ITextStoreACP::GetStatus
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onstatuschange">ITextStoreACPSink::OnStatusChange
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getstatus">ITextStoreAnchor::GetStatus
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onstatuschange">ITextStoreAnchorSink::OnStatusChange
      </a>