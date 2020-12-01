---
UID: NC:wofapi.WofEnumEntryProc
title: WofEnumEntryProc (wofapi.h)
description: Callback function that gets called for each data source in response to a call to WofEnumEntries.
helpviewer_keywords: ["WofEnumEntryProc","WofEnumEntryProc callback","WofEnumEntryProc callback function [Files]","fs.wofenumentryproc","wofapi/WofEnumEntryProc"]
old-location: fs\wofenumentryproc.htm
tech.root: fs
ms.assetid: B0569A28-7B5F-451D-A972-89A6D42F9821
ms.date: 12/05/2018
ms.keywords: WofEnumEntryProc, WofEnumEntryProc callback, WofEnumEntryProc callback function [Files], fs.wofenumentryproc, wofapi/WofEnumEntryProc
req.header: wofapi.h
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
 - WofEnumEntryProc
 - wofapi/WofEnumEntryProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wofapi.h
api_name:
 - WofEnumEntryProc
---

# WofEnumEntryProc callback function


## -description

Callback function that gets called for each data source in response to a call to <a href="/windows/desktop/api/wofapi/nf-wofapi-wofenumentries">WofEnumEntries</a>.

## -parameters

### -param EntryInfo [in]

The structure that contains specific provider info. The Type of <i>EntryInfo</i> is provider-specific.  For WOF_PROVIDER_WIM,
it will be PWIM_ENTRY_INFO.

### -param UserData [in, optional]

Optional user defined data specified in the call to <a href="/windows/desktop/api/wofapi/nf-wofapi-wofenumentries">WofEnumEntries</a>.

## -returns

A boolean value that indicates whether the enumeration was successful. The enumeration will stop if this callback function returns FALSE.