---
UID: NF:dde.FreeDDElParam
title: FreeDDElParam function (dde.h)
description: Frees the memory specified by the lParam parameter of a posted Dynamic Data Exchange (DDE) message. An application receiving a posted DDE message should call this function after it has used the UnpackDDElParam function to unpack the lParam value.
helpviewer_keywords: ["FreeDDElParam","FreeDDElParam function [Data Exchange]","_win32_FreeDDElParam","_win32_freeddelparam_cpp","dataxchg.freeddelparam","dde/FreeDDElParam","winui._win32_freeddelparam"]
old-location: dataxchg\freeddelparam.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\freeddelparam.htm
ms.date: 12/05/2018
ms.keywords: FreeDDElParam, FreeDDElParam function [Data Exchange], _win32_FreeDDElParam, _win32_freeddelparam_cpp, dataxchg.freeddelparam, dde/FreeDDElParam, winui._win32_freeddelparam
req.header: dde.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeDDElParam
 - dde/FreeDDElParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-dde-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-L1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-3-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - FreeDDElParam
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# FreeDDElParam function


## -description

Frees the memory specified by the 
			<i>lParam</i> parameter of a posted Dynamic Data Exchange (DDE) message. An application receiving a posted DDE message should call this function after it has used the <a href="/windows/desktop/api/dde/nf-dde-unpackddelparam">UnpackDDElParam</a> function to unpack the 
			<i>lParam</i> value.

## -parameters

### -param msg [in]

Type: <b>UINT</b>

The posted DDE message.

### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

An application should call this function only for posted DDE messages. 

This function frees the memory specified by the 
				<i>lParam</i> parameter. It does not free the contents of 
				<i>lParam</i>.

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/dde/nf-dde-packddelparam">PackDDElParam</a>



<b>Reference</b>



<a href="/windows/desktop/api/dde/nf-dde-reuseddelparam">ReuseDDElParam</a>



<a href="/windows/desktop/api/dde/nf-dde-unpackddelparam">UnpackDDElParam</a>
