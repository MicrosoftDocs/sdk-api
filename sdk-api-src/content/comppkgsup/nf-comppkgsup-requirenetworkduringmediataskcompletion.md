---
UID: NF:comppkgsup.RequireNetworkDuringMediaTaskCompletion
title: RequireNetworkDuringMediaTaskCompletion function
author: windows-sdk-content
description: Increments or decrements the count of network connections required for media task completion.
old-location: winprog\requirenetworkduringmediataskcompletion.htm
tech.root: devnotes
ms.assetid: D3A1E926-CC9C-4E5E-B588-A45B2FEE9FAF
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: RequireNetworkDuringMediaTaskCompletion, RequireNetworkDuringMediaTaskCompletion function [Windows API], comppkgsup/RequireNetworkDuringMediaTaskCompletion, winprog.requirenetworkduringmediataskcompletion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - RequireNetworkDuringMediaTaskCompletion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RequireNetworkDuringMediaTaskCompletion function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Increments or decrements the count of network connections required for media task completion.


## -parameters




### -param requireNetwork

If true is specified, the system's count of required network connections is incremented by one. If false is specified, the system's count of required network connections is decremented by one.


### -param requireCount [out, optional]

When provided, this parameter is populated with the current number of required network connections tracked by the system.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



