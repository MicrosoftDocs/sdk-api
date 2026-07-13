---
UID: NS:textstor.TS_STATUS
title: TS_STATUS (textstor.h)
description: The TS_STATUS structure contains document status data.
helpviewer_keywords: ["TS_STATUS","TS_STATUS structure [Text Services Framework]","_tsf_ts_status_ref","textstor/TS_STATUS","tsf.ts_status"]
old-location: tsf\ts_status.htm
tech.root: TSF
ms.assetid: d27d81f2-8599-4b65-866b-4e8fd2f589f5
ms.date: 09/06/2025
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

The **TS_STATUS** structure contains document status data.

## -struct-fields

### -field dwDynamicFlags

Contains a set of flags that can be changed by an app at run time. For example, an app can enable a check box for the user to reset the document status. This member can contain zero, or one or more of the following values.

| Value           | Meaning                    |
|-----------------|----------------------------|
| TS_SD_LOADING   | The document is loading.   |
| TS_SD_READONLY  | The document is read-only. |

### -field dwStaticFlags

Contains a set of flags that cannot be changed at run time. This member can contain zero, or one or more of the following values.

| Value                         | Meaning                                                                                  |
|-------------------------------|------------------------------------------------------------------------------------------|
| TS_SS_DISJOINTSEL             | The document supports multiple selections.                                               |
| TS_SS_REGIONS                 | The document can contain multiple regions.                                               |
| TS_SS_TRANSITORY              | The document is expected to have a short usage cycle.                                    |
| TS_SS_NOHIDDENTEXT            | The document will never contain hidden text.                                             |
| TS_SS_TKBAUTOCORRECTENABLE    | **Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard. |
| TS_SS_TKBPREDICTIONENABLE     | **Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.   |

## -remarks

The <a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS</a> structure contains document status data.


<a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS</a> is an alias for **TS_STATUS**.

**dwDynamicFlags** contains a set of flags that can be changed by an app at run time. For example, an app can enable a check box for the user to reset the status of documentation. This member can contain zero, or one or more of the following values.

| Value                      | Meaning                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TF_SD_LOADING              | The document is loading.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| TF_SD_READONLY             | The document is read-only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| TS_SD_INPUTPANEMANUALDISPLAYENABLE | The system does not attempt automatic touch keyboard invocation when the control is touched.  Instead, the app calls [TryShow(CoreInputViewKind)](/uwp/api/windows.ui.viewmanagement.core.coreinputview.tryshow) to show the keyboard when appropriate (the app should monitor input to select the [CoreInputViewKind](/uwp/api/windows.ui.viewmanagement.core.coreinputviewkind)). |
| TS_SD_UIINTEGRATIONENABLE  | **Starting with Windows 8.1:** The text control owning the document sets this flag to indicate its support of Input Method Editor (IME) UI integration. When specified, the IME should attempt to align the candidate window below the text box instead of floating near the cursor.<br>**Note:** Not all IMEs respond to this flag. IME candidate lists are positioned on the screen with sufficient size to allow basic text input. In some cases, the IME may enforce a reasonable minimum size.  An IME might also choose to adjust the candidate window and keyboard input behavior to provide a better user experience, such as using a horizontal candidate list and allowing some keys such as up arrow and down arrow to be sent to the app for scenarios such as suggestion list navigation. |
| TF_SD_TKBAUTOCORRECTENABLE | **Starting with Windows 8.1:** The document supports autocorrection provided by the touch keyboard. This support can change during the lifetime of the control.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| TF_SD_TKBPREDICTIONENABLE  | **Starting with Windows 8.1:** The document supports text suggestions provided by the touch keyboard. This support can change during the lifetime of the control.                                                                                                                                                                                                                                                                                                                                                                                                                                    |

**dwStaticFlags** contains a set of flags that cannot be changed at run time. This member can contain zero, or one or more of the following values.

| Value                         | Meaning                                                                                  |
|-------------------------------|------------------------------------------------------------------------------------------|
| TF_SS_DISJOINTSEL | The document supports multiple selections. |
| TF_SS_REGIONS | The document can contain multiple regions. |
| TF_SS_TRANSITORY | The document is expected to have a short usage cycle. |
| TF_SS_TKBAUTOCORRECTENABLE | **Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard. |
| TF_SS_TKBPREDICTIONENABLE | **Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard. |


## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getstatus">ITextStoreACP::GetStatus
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onstatuschange">ITextStoreACPSink::OnStatusChange
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getstatus">ITextStoreAnchor::GetStatus
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onstatuschange">ITextStoreAnchorSink::OnStatusChange
      </a>