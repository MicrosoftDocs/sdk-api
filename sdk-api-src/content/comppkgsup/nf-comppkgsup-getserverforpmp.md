---
UID: NF:comppkgsup.GetServerForPMP
title: GetServerForPMP function (comppkgsup.h)
author: windows-sdk-content
description: Gets a COM server that has been registered for Protected Media Process (PMP) usage with previous call to RegisterServerForPMP.
old-location: winprog\getserverforpmp.htm
tech.root: DevNotes
ms.assetid: 0E343396-A294-45E3-88E5-9B63EB8B10B9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetServerForPMP, GetServerForPMP function [Windows API], comppkgsup/GetServerForPMP, winprog.getserverforpmp
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
 - GetServerForPMP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetServerForPMP function


## -description


Gets a  COM server that has been registered  for Protected Media Process (PMP) usage with previous call to <a href="https://msdn.microsoft.com/F18A5596-F21E-427B-8281-544DD7CA9E0B">RegisterServerForPMP</a>.


## -parameters




### -param serverClassId

The CLSID of the server to be retrieved.


### -param unknown [out]

Receives a pointer to the requested COM server interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



