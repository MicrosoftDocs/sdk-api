---
UID: NS:ddeml.tagMONHSZSTRUCTA
title: tagMONHSZSTRUCTA
author: windows-sdk-content
description: Contains information about a Dynamic Data Exchange (DDE) string handle. A DDE monitoring application can use this structure when monitoring the activity of the string manager component of the DDE Management Library.
old-location: dataxchg\monhszstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monhszstruct.htm
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "*PMONHSZSTRUCTA, MH_CLEANUP, MH_CREATE, MH_DELETE, MH_KEEP, MONHSZSTRUCT, MONHSZSTRUCT structure [Data Exchange], MONHSZSTRUCTA, MONHSZSTRUCTW, PMONHSZSTRUCT, PMONHSZSTRUCT structure pointer [Data Exchange], _win32_MONHSZSTRUCT_str, _win32_monhszstruct_str_cpp, dataxchg.monhszstruct_str, ddeml/MONHSZSTRUCT, ddeml/MONHSZSTRUCTA, ddeml/MONHSZSTRUCTW, ddeml/PMONHSZSTRUCT, tagMONHSZSTRUCTA, winui._win32_monhszstruct_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: MONHSZSTRUCTA, *PMONHSZSTRUCTA
req.redist: 
---

# tagMONHSZSTRUCTA structure


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
An application is freeing its DDE resources, causing the system to delete string handles the application had created. (The application called the <a href="https://msdn.microsoft.com/0997c135-c915-4a9c-953c-80657589795e">DdeUninitialize</a> function.)

</td>
</tr>
<tr>
<td width="40%"><a id="MH_CREATE"></a><a id="mh_create"></a><dl>
<dt><b>MH_CREATE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
An application is creating a string handle. (The application called the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function.)

</td>
</tr>
<tr>
<td width="40%"><a id="MH_DELETE"></a><a id="mh_delete"></a><dl>
<dt><b>MH_DELETE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
An application is deleting a string handle. (The application called the <a href="https://msdn.microsoft.com/93228467-345b-4ff1-942e-2d75a53bce65">DdeFreeStringHandle</a> function.)

</td>
</tr>
<tr>
<td width="40%"><a id="MH_KEEP"></a><a id="mh_keep"></a><dl>
<dt><b>MH_KEEP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An application is increasing the usage count of a string handle. (The application called the <a href="https://msdn.microsoft.com/ecef0207-061c-451a-a911-1b821bbe099d">DdeKeepStringHandle</a> function.)

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



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/65bea5e0-ab86-4e00-9dbf-9809aab18616">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/24fe9042-7b9f-4139-a9b5-d8c72529d897">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/4e7647a0-c41e-4ec9-b441-01538e83aca3">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/7d971b35-0c88-42c3-83b9-93d5de6c95f9">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

