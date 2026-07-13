---
UID: NF:dde.ReuseDDElParam
title: ReuseDDElParam function (dde.h)
description: Enables an application to reuse a packed Dynamic Data Exchange (DDE) lParam parameter, rather than allocating a new packed lParam. Using this function reduces reallocations for applications that pass packed DDE messages.
helpviewer_keywords: ["ReuseDDElParam","ReuseDDElParam function [Data Exchange]","_win32_ReuseDDElParam","_win32_reuseddelparam_cpp","dataxchg.reuseddelparam","dde/ReuseDDElParam","winui._win32_reuseddelparam"]
old-location: dataxchg\reuseddelparam.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\reuseddelparam.htm
ms.date: 12/05/2018
ms.keywords: ReuseDDElParam, ReuseDDElParam function [Data Exchange], _win32_ReuseDDElParam, _win32_reuseddelparam_cpp, dataxchg.reuseddelparam, dde/ReuseDDElParam, winui._win32_reuseddelparam
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
 - ReuseDDElParam
 - dde/ReuseDDElParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-dde-l1-1-0.dll
 - User32.dll
api_name:
 - ReuseDDElParam
---

# ReuseDDElParam function


## -description

Enables an application to reuse a packed Dynamic Data Exchange (DDE) <i>lParam</i> parameter, rather than allocating a new packed 
			<i>lParam</i>. Using this function reduces reallocations for applications that pass packed DDE messages.

## -parameters

### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message being reused.

### -param msgIn [in]

Type: <b>UINT</b>

The identifier of the received DDE message.

### -param msgOut [in]

Type: <b>UINT</b>

The identifier of the DDE message to be posted. The DDE message will reuse the packed 
					<i>lParam</i> parameter.

### -param uiLo [in]

Type: <b>UINT_PTR</b>

The value to be packed into the low-order word of the reused 
					<i>lParam</i> parameter.

### -param uiHi [in]

Type: <b>UINT_PTR</b>

The value to be packed into the high-order word of the reused 
					<i>lParam</i> parameter.

## -returns

Type: <b>LPARAM</b>

The return value is the new 
						<i>lParam</i> value.

## -remarks

The return value must be posted as the 
				<i>lParam</i> parameter of a DDE message; it must not be used for any other purpose. Once the return value is posted, the posting application need not perform any action to dispose of the 
				<i>lParam</i> parameter. 

Use <b>ReuseDDElParam</b> instead of <a href="/windows/desktop/api/dde/nf-dde-freeddelparam">FreeDDElParam</a> if the 
				<i>lParam</i> parameter will be reused in a responding message. <b>ReuseDDElParam</b> returns the 
				<i>lParam</i> appropriate for reuse. 

This function allocates or frees 
				<i>lParam</i> parameters as needed, depending on the packing requirements of the incoming and outgoing messages. This reduces reallocations in passing DDE messages.

## -see-also

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/dde/nf-dde-freeddelparam">FreeDDElParam</a>



<a href="/windows/desktop/api/dde/nf-dde-packddelparam">PackDDElParam</a>



<b>Reference</b>



<a href="/windows/desktop/api/dde/nf-dde-unpackddelparam">UnpackDDElParam</a>