---
UID: NF:shdeprecated.ITravelLog.CountEntries
title: ITravelLog::CountEntries (shdeprecated.h)
description: Deprecated. Generates the number of entries in the travel log.
helpviewer_keywords: ["CountEntries","CountEntries method [Windows Shell]","CountEntries method [Windows Shell]","ITravelLog interface","ITravelLog interface [Windows Shell]","CountEntries method","ITravelLog.CountEntries","ITravelLog::CountEntries","shdeprecated/ITravelLog::CountEntries","shell.ITravelLog_CountEntries","zone_ITravelLog_CountEntries"]
old-location: shell\ITravelLog_CountEntries.htm
tech.root: shell
ms.assetid: 490f7350-6c67-4c79-a100-af266b269472
ms.date: 12/05/2018
ms.keywords: CountEntries, CountEntries method [Windows Shell], CountEntries method [Windows Shell],ITravelLog interface, ITravelLog interface [Windows Shell],CountEntries method, ITravelLog.CountEntries, ITravelLog::CountEntries, shdeprecated/ITravelLog::CountEntries, shell.ITravelLog_CountEntries, zone_ITravelLog_CountEntries
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - ITravelLog::CountEntries
 - shdeprecated/ITravelLog::CountEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelLog.CountEntries
---

# ITravelLog::CountEntries


## -description

Deprecated. Generates the number of entries in the travel log.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.

## -returns

Type: <b>DWORD</b>

The number of entries in the travel log.