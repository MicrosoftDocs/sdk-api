---
UID: NF:comppkgsup.RegisterServerForPMP
title: RegisterServerForPMP function
author: windows-sdk-content
description: Registers a COM Server CLSID and a class factory for Protected Media Process (PMP) usage.
old-location: winprog\registerserverforpmp.htm
tech.root: devnotes
ms.assetid: F18A5596-F21E-427B-8281-544DD7CA9E0B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegisterServerForPMP, RegisterServerForPMP function [Windows API], comppkgsup/RegisterServerForPMP, winprog.registerserverforpmp
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
 - RegisterServerForPMP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterServerForPMP function


## -description


Registers a COM Server CLSID and a class factory for Protected Media Process (PMP) usage.


## -parameters




### -param serverClassId

The CLSID of the COM server to be registered.


### -param classFactory

The class factory to be registered.


### -param token [out]

Receives a pointer to a registration token that can be used to unregister the server with <a href="https://msdn.microsoft.com/FF89301E-FE17-4B14-872E-271BDB85A784">UnregisterServerForPMP</a>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



