---
UID: NE:dshowasf._AM_ASFWRITERCONFIG_PARAM
title: "_AM_ASFWRITERCONFIG_PARAM (dshowasf.h)"
description: The _AM_ASFWRITERCONFIG_PARAM DirectShow QASF enumeration type defines filter configuration parameters used in the IConfigAsfWriter2::GetParam and SetParam methods.
helpviewer_keywords: ["AM_CONFIGASFWRITER_PARAM_AUTOINDEX","AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS","AM_CONFIGASFWRITER_PARAM_MULTIPASS","_AM_ASFWRITERCONFIG_PARAM","_AM_ASFWRITERCONFIG_PARAM enumeration [windows Media Format]","dshowasf/AM_CONFIGASFWRITER_PARAM_AUTOINDEX","dshowasf/AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS","dshowasf/AM_CONFIGASFWRITER_PARAM_MULTIPASS","dshowasf/_AM_ASFWRITERCONFIG_PARAM","wmformat._am_asfwriterconfig_param_enumeration"]
old-location: wmformat\_am_asfwriterconfig_param_enumeration.htm
tech.root: wmformat
ms.assetid: 773f9b98-8b88-4b2d-b1f0-40bb1e0c0ab0
ms.date: 12/05/2018
ms.keywords: AM_CONFIGASFWRITER_PARAM_AUTOINDEX, AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS, AM_CONFIGASFWRITER_PARAM_MULTIPASS, _AM_ASFWRITERCONFIG_PARAM, _AM_ASFWRITERCONFIG_PARAM enumeration [windows Media Format], dshowasf/AM_CONFIGASFWRITER_PARAM_AUTOINDEX, dshowasf/AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS, dshowasf/AM_CONFIGASFWRITER_PARAM_MULTIPASS, dshowasf/_AM_ASFWRITERCONFIG_PARAM, wmformat._am_asfwriterconfig_param_enumeration
req.header: dshowasf.h
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
 - _AM_ASFWRITERCONFIG_PARAM
 - dshowasf/_AM_ASFWRITERCONFIG_PARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dshowasf.h
api_name:
 - _AM_ASFWRITERCONFIG_PARAM
---

# _AM_ASFWRITERCONFIG_PARAM enumeration


## -description

The <b>_AM_ASFWRITERCONFIG_PARAM</b> DirectShow QASF enumeration type defines filter configuration parameters used in the <a href="/windows/desktop/wmformat/iconfigasfwriter2-getparam">IConfigAsfWriter2::GetParam</a> and <a href="/windows/desktop/wmformat/iconfigasfwriter2-setparam">SetParam</a> methods.

## -enum-fields

### -field AM_CONFIGASFWRITER_PARAM_AUTOINDEX:1

Indicates whether the <a href="/windows/desktop/wmformat/wm-asf-writer-filter">WM ASF Writer</a> should automatically create a temporal index after it has completed encoding a file. Set this parameter to <b>FALSE</b> if you want to create a frame-based index using the Windows Media Format SDK directly.

### -field AM_CONFIGASFWRITER_PARAM_MULTIPASS

Indicates whether the filter should operate in two-pass mode. See Remarks.

### -field AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS

Indicates that the <a href="/windows/desktop/wmformat/wm-asf-writer-filter">WM ASF Writer</a> will not attempt to compress the input streams. Use this flag to pack content that is not Windows Media–based into an ASF file.

## -remarks

In two-pass mode the filter makes two passes through the file. In the first pass, the filter examines each media stream in its entirety to determine the optimal encoding parameters for the file. The actual encoding is performed in the second pass. Therefore, to create an ASF file in two-pass mode, you must run the graph, wait for an <b>EC_PREPROCESS_COMPLETE</b> event, seek to the beginning of the source file, and then run the graph a second time.

<div class="alert"><b>Important</b>  To receive the <b>EC_PREPROCESS_COMPLETE</b> event you must use the DirectShow <b>GetEvent</b> method as demonstrated in the DSCopy sample. The DirectShow <b>WaitForCompletion</b> method will not receive this particular event.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/wmformat/configuring-profiles-and-other-file-properties--qasf">Configuring Profiles and Other File Properties (QASF)</a>



<a href="/windows/desktop/wmformat/directshow-qasf-reference">DirectShow QASF Reference</a>



<a href="/windows/desktop/wmformat/iconfigasfwriter2-getparam">IConfigAsfWriter2::GetParam</a>



<a href="/windows/desktop/wmformat/iconfigasfwriter2-setparam">IConfigAsfWriter2::SetParam</a>
