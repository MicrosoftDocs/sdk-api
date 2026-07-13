---
UID: NS:ddeml.tagMONHSZSTRUCTW
title: MONHSZSTRUCTW (ddeml.h)
description: Contains information about a Dynamic Data Exchange (DDE) string handle. A DDE monitoring application can use this structure when monitoring the activity of the string manager component of the DDE Management Library. (Unicode)
helpviewer_keywords: ["*PMONHSZSTRUCTW","MH_CLEANUP","MH_CREATE","MH_DELETE","MH_KEEP","MONHSZSTRUCT","MONHSZSTRUCT structure [Data Exchange]","MONHSZSTRUCTA","MONHSZSTRUCTW","PMONHSZSTRUCT","PMONHSZSTRUCT structure pointer [Data Exchange]","_win32_MONHSZSTRUCT_str","_win32_monhszstruct_str_cpp","dataxchg.monhszstruct_str","ddeml/MONHSZSTRUCT","ddeml/MONHSZSTRUCTA","ddeml/MONHSZSTRUCTW","ddeml/PMONHSZSTRUCT","winui._win32_monhszstruct_str"]
old-location: dataxchg\monhszstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monhszstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMONHSZSTRUCTW, MH_CLEANUP, MH_CREATE, MH_DELETE, MH_KEEP, MONHSZSTRUCT, MONHSZSTRUCT structure [Data Exchange], MONHSZSTRUCTA, MONHSZSTRUCTW, PMONHSZSTRUCT, PMONHSZSTRUCT structure pointer [Data Exchange], _win32_MONHSZSTRUCT_str, _win32_monhszstruct_str_cpp, dataxchg.monhszstruct_str, ddeml/MONHSZSTRUCT, ddeml/MONHSZSTRUCTA, ddeml/MONHSZSTRUCTW, ddeml/PMONHSZSTRUCT, winui._win32_monhszstruct_str'
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MONHSZSTRUCTW (Unicode) and MONHSZSTRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MONHSZSTRUCTW, *PMONHSZSTRUCTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONHSZSTRUCTW
 - ddeml/tagMONHSZSTRUCTW
 - PMONHSZSTRUCTW
 - ddeml/PMONHSZSTRUCTW
 - MONHSZSTRUCTW
 - ddeml/MONHSZSTRUCTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - MONHSZSTRUCT
 - MONHSZSTRUCTA
 - MONHSZSTRUCTW
---

# MONHSZSTRUCTW structure


## -description

Contains information about a Dynamic Data Exchange (DDE) string handle. A DDE monitoring application can use this structure when monitoring the activity of the string manager component of the DDE Management Library.

## -struct-fields

### -field cb

Type: <b>UINT</b>

The structure's size, in bytes.

### -field fsAction

Type: <b>BOOL</b>

The action being performed on the string identified by the <b>hsz</b> member. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MH_CLEANUP"></a><a id="mh_cleanup"></a><dl>
<dt><b>MH_CLEANUP</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
An application is freeing its DDE resources, causing the system to delete string handles the application had created. (The application called the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeuninitialize">DdeUninitialize</a> function.)

</td>
</tr>
<tr>
<td width="40%"><a id="MH_CREATE"></a><a id="mh_create"></a><dl>
<dt><b>MH_CREATE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
An application is creating a string handle. (The application called the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a> function.)

</td>
</tr>
<tr>
<td width="40%"><a id="MH_DELETE"></a><a id="mh_delete"></a><dl>
<dt><b>MH_DELETE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
An application is deleting a string handle. (The application called the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreestringhandle">DdeFreeStringHandle</a> function.)

</td>
</tr>
<tr>
<td width="40%"><a id="MH_KEEP"></a><a id="mh_keep"></a><dl>
<dt><b>MH_KEEP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An application is increasing the usage count of a string handle. (The application called the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddekeepstringhandle">DdeKeepStringHandle</a> function.)

</td>
</tr>
</table>

### -field dwTime

Type: <b>DWORD</b>

The Windows time at which the action specified by the <b>fsAction</b> member takes place. Windows time is the number of milliseconds that have elapsed since the system was booted.

### -field hsz

Type: <b>HSZ</b>

A handle to the string. Because string handles are local to the process, this member is a global atom.

### -field hTask

Type: <b>HANDLE</b>

A handle to the task (application instance) performing the action on the string handle.

### -field str

Type: <b>TCHAR[1]</b>

Pointer to the string identified by the <b>hsz</b> member.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-moncbstruct">MONCBSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monconvstruct">MONCONVSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monerrstruct">MONERRSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monlinkstruct">MONLINKSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monmsgstruct">MONMSGSTRUCT</a>



<b>Reference</b>

## -remarks

> [!NOTE]
> The ddeml.h header defines MONHSZSTRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
