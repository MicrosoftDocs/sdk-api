---
UID: NS:pdh._PDH_COUNTER_INFO_A
title: PDH_COUNTER_INFO_A (pdh.h)
description: The PDH_COUNTER_INFO structure contains information describing the properties of a counter. This information also includes the counter path. (ANSI)
helpviewer_keywords: ["*PPDH_COUNTER_INFO_A","PDH_COUNTER_INFO","PDH_COUNTER_INFO structure [Perf]","PDH_COUNTER_INFO_A","PDH_COUNTER_INFO_W","PPDH_COUNTER_INFO","PPDH_COUNTER_INFO structure pointer [Perf]","_win32_pdh_counter_info_str","base.pdh_counter_info_str","pdh/PDH_COUNTER_INFO","pdh/PDH_COUNTER_INFO_A","pdh/PDH_COUNTER_INFO_W","pdh/PPDH_COUNTER_INFO","perf.pdh_counter_info_str"]
old-location: perf\pdh_counter_info_str.htm
tech.root: perf
ms.assetid: c9ede50e-85de-4a68-b539-54285c2599cb
ms.date: 12/05/2018
ms.keywords: '*PPDH_COUNTER_INFO_A, PDH_COUNTER_INFO, PDH_COUNTER_INFO structure [Perf], PDH_COUNTER_INFO_A, PDH_COUNTER_INFO_W, PPDH_COUNTER_INFO, PPDH_COUNTER_INFO structure pointer [Perf], _win32_pdh_counter_info_str, base.pdh_counter_info_str, pdh/PDH_COUNTER_INFO, pdh/PDH_COUNTER_INFO_A, pdh/PDH_COUNTER_INFO_W, pdh/PPDH_COUNTER_INFO, perf.pdh_counter_info_str'
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PDH_COUNTER_INFO_W (Unicode) and PDH_COUNTER_INFO_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PDH_COUNTER_INFO_A, *PPDH_COUNTER_INFO_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_COUNTER_INFO_A
 - pdh/_PDH_COUNTER_INFO_A
 - PPDH_COUNTER_INFO_A
 - pdh/PPDH_COUNTER_INFO_A
 - PDH_COUNTER_INFO_A
 - pdh/PDH_COUNTER_INFO_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_COUNTER_INFO
 - PDH_COUNTER_INFO_A
 - PDH_COUNTER_INFO_W
---

# PDH_COUNTER_INFO_A structure


## -description

The 
<b>PDH_COUNTER_INFO</b> structure contains information describing the properties of a counter. This information also includes the counter path.

## -struct-fields

### -field dwLength

Size of the structure, including the appended strings, in bytes.

### -field dwType

Counter type. For a list of counter types, see the Counter Types section of the <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Windows Server 2003 Deployment Kit</a>. The counter type constants are defined in Winperf.h.

### -field CVersion

Counter version information.
					Not used.

### -field CStatus

Counter status that indicates if the counter value is valid. For a list of possible values, see 
<a href="/windows/desktop/PerfCtrs/checking-pdh-interface-return-values">Checking PDH Interface Return Values</a>.

### -field lScale

Scale factor to use when computing the displayable value of the counter.
					The scale factor is a power of ten. The valid range of this parameter is PDH_MIN_SCALE (–7) (the returned value is the actual value times 10<sup>–</sup>⁷) to PDH_MAX_SCALE (+7) (the returned value is the actual value times 10⁺⁷). A value of zero will set the scale to one, so that the actual value is returned

### -field lDefaultScale

Default scale factor as suggested by the counter's provider.

### -field dwUserData

The value passed in the <i>dwUserData</i> parameter when calling <a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a>.

### -field dwQueryUserData

The value passed in the <i>dwUserData</i> parameter when calling <a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>.

### -field szFullPath

<b>Null</b>-terminated string that specifies the full counter path. The string follows this structure in memory.

### -field DataItemPath

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_data_item_path_elements_a">PDH_DATA_ITEM_PATH_ELEMENTS</a> structure. Not used.

### -field CounterPath

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a> structure.

### -field szMachineName

<b>Null</b>-terminated string that contains the name of the computer specified in the counter path. Is <b>NULL</b>, if the path does not specify a computer. The string follows this structure in memory.

### -field szObjectName

<b>Null</b>-terminated string that contains the name of the performance object specified in the counter path. The string follows this structure in memory.

### -field szInstanceName

<b>Null</b>-terminated string that contains the name of the object instance specified in the counter path. Is <b>NULL</b>, if the path does not specify an instance. The string follows this structure in memory.

### -field szParentInstance

<b>Null</b>-terminated string that contains the name of the parent instance specified in the counter path. Is <b>NULL</b>, if the path does not specify a parent instance. The string follows this structure in memory.

### -field dwInstanceIndex

Instance index specified in the counter path. Is 0, if the path does not specify an instance index.

### -field szCounterName

<b>Null</b>-terminated string that contains the counter name. The string follows this structure in memory.

### -field szExplainText

Help text that describes the counter. Is <b>NULL</b> if the source is a log file.

### -field DataBuffer

Start of the string data that is appended to the structure.

## -remarks

When you allocate memory for this structure, allocate enough memory for the member strings, such as <b>szCounterName</b>, that are appended to the end of this structure.

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a>



<a href="/windows/desktop/api/pdh/ns-pdh-pdh_data_item_path_elements_a">PDH_DATA_ITEM_PATH_ELEMENTS</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a>
