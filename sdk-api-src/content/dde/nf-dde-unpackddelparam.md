---
UID: NF:dde.UnpackDDElParam
title: UnpackDDElParam function (dde.h)
description: Unpacks a Dynamic Data Exchange (DDE)lParam value received from a posted DDE message.
helpviewer_keywords: ["UnpackDDElParam","UnpackDDElParam function [Data Exchange]","_win32_UnpackDDElParam","_win32_unpackddelparam_cpp","dataxchg.unpackddelparam","dde/UnpackDDElParam","winui._win32_unpackddelparam"]
old-location: dataxchg\unpackddelparam.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\unpackddelparam.htm
ms.date: 12/05/2018
ms.keywords: UnpackDDElParam, UnpackDDElParam function [Data Exchange], _win32_UnpackDDElParam, _win32_unpackddelparam_cpp, dataxchg.unpackddelparam, dde/UnpackDDElParam, winui._win32_unpackddelparam
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
 - UnpackDDElParam
 - dde/UnpackDDElParam
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
 - UnpackDDElParam
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# UnpackDDElParam function


## -description

Unpacks a Dynamic Data Exchange (DDE)<i>lParam</i> value received from a posted DDE message.

## -parameters

### -param msg [in]

Type: <b>UINT</b>

The posted DDE message.

### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message that was received. The application must free the memory object specified by the 
					<i>lParam</i> parameter by calling the <a href="/windows/desktop/api/dde/nf-dde-freeddelparam">FreeDDElParam</a> function.

### -param puiLo [out]

Type: <b>PUINT_PTR</b>

A pointer to a variable that receives the low-order word of 
					<i>lParam</i>.

### -param puiHi [out]

Type: <b>PUINT_PTR</b>

A pointer to a variable that receives the high-order word of 
					<i>lParam</i>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

<a href="/windows/desktop/api/dde/nf-dde-packddelparam">PackDDElParam</a> eases the porting of 16-bit DDE applications to 32-bit DDE applications.

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/dde/nf-dde-freeddelparam">FreeDDElParam</a>



<a href="/windows/desktop/api/dde/nf-dde-packddelparam">PackDDElParam</a>



<b>Reference</b>



<a href="/windows/desktop/api/dde/nf-dde-reuseddelparam">ReuseDDElParam</a>
