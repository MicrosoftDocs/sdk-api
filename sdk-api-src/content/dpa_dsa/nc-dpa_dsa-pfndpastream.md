---
UID: NC:dpa_dsa.PFNDPASTREAM
title: PFNDPASTREAM (dpa_dsa.h)

description: Defines the prototype for the callback function used by DPA_LoadStream and DPA_SaveStream.
old-location: controls\PFNDPASTREAM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\pfndpastream.htm

ms.date: 12/05/2018
ms.keywords: PFNDPASTREAM, PFNDPASTREAM callback, PFNDPASTREAM callback function [Windows Controls], _win32_PFNDPASTREAM_Function, _win32_PFNDPASTREAM_Function_cpp, controls.PFNDPASTREAM, controls._win32_PFNDPASTREAM_Function, dpa_dsa/PFNDPASTREAM
ms.topic: callback
f1_keywords:
- dpa_dsa/PFNDPASTREAM
dev_langs:
 - c++
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- dpa_dsa.h
api_name:
- PFNDPASTREAM
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFNDPASTREAM callback function


## -description


Defines the prototype for the callback function used by <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream">DPA_LoadStream</a> and <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream">DPA_SaveStream</a>.


## -parameters




### -param *pinfo [in]

Type: <b>DPASTREAMINFO*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/ns-dpa_dsa-dpastreaminfo">DPASTREAMINFO</a> structure.


### -param *pstream [in]

Type: <b>struct IStream*</b>

An <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object to read from or write to.


### -param *pvInstData [in, optional]

Type: <b>void*</b>

A void pointer to callback data that the client passed to <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream">DPA_LoadStream</a> or <a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream">DPA_SaveStream</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



