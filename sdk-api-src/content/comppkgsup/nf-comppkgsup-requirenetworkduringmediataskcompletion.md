---
UID: NF:comppkgsup.RequireNetworkDuringMediaTaskCompletion
title: RequireNetworkDuringMediaTaskCompletion function (comppkgsup.h)
description: Increments or decrements the count of network connections required for media task completion.
helpviewer_keywords: ["RequireNetworkDuringMediaTaskCompletion","RequireNetworkDuringMediaTaskCompletion function [Windows API]","comppkgsup/RequireNetworkDuringMediaTaskCompletion","winprog.requirenetworkduringmediataskcompletion"]
old-location: winprog\requirenetworkduringmediataskcompletion.htm
tech.root: winprog
ms.assetid: D3A1E926-CC9C-4E5E-B588-A45B2FEE9FAF
ms.date: 12/05/2018
ms.keywords: RequireNetworkDuringMediaTaskCompletion, RequireNetworkDuringMediaTaskCompletion function [Windows API], comppkgsup/RequireNetworkDuringMediaTaskCompletion, winprog.requirenetworkduringmediataskcompletion
req.header: comppkgsup.h
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
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RequireNetworkDuringMediaTaskCompletion
 - comppkgsup/RequireNetworkDuringMediaTaskCompletion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - RequireNetworkDuringMediaTaskCompletion
---

# RequireNetworkDuringMediaTaskCompletion function


## -description

Increments or decrements the count of network connections required for media task completion.

## -parameters

### -param requireNetwork

If true is specified, the system's count of required network connections is incremented by one. If false is specified, the system's count of required network connections is decremented by one.

### -param requireCount [out, optional]

When provided, this parameter is populated with the current number of required network connections tracked by the system.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

