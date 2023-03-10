---
UID: NF:werapi.WerReportSetParameter
title: WerReportSetParameter function (werapi.h)
description: Sets the parameters that uniquely identify an event for the specified report.
helpviewer_keywords: ["WER_P0","WER_P1","WER_P2","WER_P3","WER_P4","WER_P5","WER_P6","WER_P7","WER_P8","WER_P9","WerReportSetParameter","WerReportSetParameter function [Windows Error Reporting]","base.werreportsetparameter","wer.werreportsetparameter","werapi/WerReportSetParameter"]
old-location: wer\werreportsetparameter.htm
tech.root: wer
ms.assetid: accf423d-6f03-41e2-b5e9-4a0b630bc918
ms.date: 12/05/2018
ms.keywords: WER_P0, WER_P1, WER_P2, WER_P3, WER_P4, WER_P5, WER_P6, WER_P7, WER_P8, WER_P9, WerReportSetParameter, WerReportSetParameter function [Windows Error Reporting], base.werreportsetparameter, wer.werreportsetparameter, werapi/WerReportSetParameter
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerReportSetParameter
 - werapi/WerReportSetParameter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportSetParameter
---

# WerReportSetParameter function


## -description

Sets the parameters that uniquely identify an event for the specified report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a> function.

### -param dwparamID [in]

The identifier of the parameter to be set. This parameter can be one of the following values.

<a id="WER_P0"></a>
<a id="wer_p0"></a>


#### WER_P0

<a id="WER_P1"></a>
<a id="wer_p1"></a>


#### WER_P1

<a id="WER_P2"></a>
<a id="wer_p2"></a>


#### WER_P2

<a id="WER_P3"></a>
<a id="wer_p3"></a>


#### WER_P3

<a id="WER_P4"></a>
<a id="wer_p4"></a>


#### WER_P4

<a id="WER_P5"></a>
<a id="wer_p5"></a>


#### WER_P5

<a id="WER_P6"></a>
<a id="wer_p6"></a>


#### WER_P6

<a id="WER_P7"></a>
<a id="wer_p7"></a>


#### WER_P7

<a id="WER_P8"></a>
<a id="wer_p8"></a>


#### WER_P8

<a id="WER_P9"></a>
<a id="wer_p9"></a>


#### WER_P9

### -param pwzName [in, optional]

A pointer to a Unicode string that contains the name of the parameter. If this parameter is <b>NULL</b>, the default name is P<i>x</i>, where <i>x</i> matches the integer portion of the value specified in <i>dwparamID</i>.

### -param pwzValue [in]

The parameter value.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_LENGTH_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The length of one or more string arguments has exceeded its limit.

</td>
</tr>
</table>

## -remarks

Each report supports parameters P0 through P9. This function sets one parameter at a time. If parameter P<i>x</i> is set, then all parameters from P0 and P<i>x</i> must be set.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>