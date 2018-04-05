---
UID: NF:comppkgsup.UnregisterServerForPMP
title: UnregisterServerForPMP function
author: windows-driver-content
description: Registers a COM Server CLSID and a class factory that were previously registered for Protected Media Process (PMP) usage.
old-location: winprog\unregisterserverforpmp.htm
old-project: DevNotes
ms.assetid: FF89301E-FE17-4B14-872E-271BDB85A784
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UnregisterServerForPMP, UnregisterServerForPMP function [Windows API], comppkgsup/UnregisterServerForPMP, winprog.unregisterserverforpmp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAGELISTDRAWPARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CompPkgSup.dll
api_name:
-	UnregisterServerForPMP
product: Windows
targetos: Windows
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
---

# UnregisterServerForPMP function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Registers a COM Server CLSID and a class factory that were previously registered for Protected Media Process (PMP) usage.


## -parameters




### -param token

The registration token obtained from a previous call to <a href="https://msdn.microsoft.com/F18A5596-F21E-427B-8281-544DD7CA9E0B">RegisterServerForPMP</a>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



