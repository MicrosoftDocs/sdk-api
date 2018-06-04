---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WerReportSetParameter function


## -description


Sets the parameters that uniquely identify an event for the specified report.


## -parameters




### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a> function.


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




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

