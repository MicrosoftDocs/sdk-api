---
UID: NF:msctf.ITfInputProcessorProfileMgr.ReleaseInputProcessor
title: ITfInputProcessorProfileMgr::ReleaseInputProcessor (msctf.h)
description: The ITfInputProcessorProfileMgr::ReleaseInputProcessor method deactivates the profiles belonging to the text services of the specified CLSID and releases the instance of ITfTextInputProcessorEx interface.
helpviewer_keywords: ["ITfInputProcessorProfileMgr interface [Text Services Framework]","ReleaseInputProcessor method","ITfInputProcessorProfileMgr.ReleaseInputProcessor","ITfInputProcessorProfileMgr::ReleaseInputProcessor","ReleaseInputProcessor","ReleaseInputProcessor method [Text Services Framework]","ReleaseInputProcessor method [Text Services Framework]","ITfInputProcessorProfileMgr interface","TF_RIP_FLAG_FREEUNUSEDLIBRARIES","msctf/ITfInputProcessorProfileMgr::ReleaseInputProcessor","tsf.itfinputprocessorprofilemgr_releaseinputprocessor"]
old-location: tsf\itfinputprocessorprofilemgr_releaseinputprocessor.htm
tech.root: TSF
ms.assetid: a7bcc50a-9f94-4a55-aca2-db9a40be2157
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileMgr interface [Text Services Framework],ReleaseInputProcessor method, ITfInputProcessorProfileMgr.ReleaseInputProcessor, ITfInputProcessorProfileMgr::ReleaseInputProcessor, ReleaseInputProcessor, ReleaseInputProcessor method [Text Services Framework], ReleaseInputProcessor method [Text Services Framework],ITfInputProcessorProfileMgr interface, TF_RIP_FLAG_FREEUNUSEDLIBRARIES, msctf/ITfInputProcessorProfileMgr::ReleaseInputProcessor, tsf.itfinputprocessorprofilemgr_releaseinputprocessor
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfileMgr::ReleaseInputProcessor
 - msctf/ITfInputProcessorProfileMgr::ReleaseInputProcessor
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
 - ITfInputProcessorProfileMgr.ReleaseInputProcessor
---

# ITfInputProcessorProfileMgr::ReleaseInputProcessor


## -description

The <b>ITfInputProcessorProfileMgr::ReleaseInputProcessor</b> method deactivates the profiles belonging to the text services of the specified CLSID and releases the instance of  <a href="/windows/desktop/api/msctf/nn-msctf-itftextinputprocessorex">ITfTextInputProcessorEx</a> interface.

## -parameters

### -param rclsid [in]

[in] CLSID of the textservice to be released.

### -param dwFlags [in]

[in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_RIP_FLAG_FREEUNUSEDLIBRARIES"></a><a id="tf_rip_flag_freeunusedlibraries"></a><dl>
<dt><b>TF_RIP_FLAG_FREEUNUSEDLIBRARIES</b></dt>
</dl>
</td>
<td width="60%">
If this bit is on, this method calls CoFreeUnusedLibrariesEx() so the text services DLL might be freed if it does not have any more COM/DLL reference. Warning: This flag could cause some other unrelated COM/DLL free.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

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