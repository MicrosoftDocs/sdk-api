---
UID: NF:shlobj.IColumnProvider.Initialize
title: IColumnProvider::Initialize
author: windows-sdk-content
description: Initializes an IColumnProvider interface.
old-location: shell\IColumnProvider_Initialize.htm
tech.root: shell
ms.assetid: 4975042d-549e-4032-9f42-468dc7e3c20e
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IColumnProvider interface [Windows Shell],Initialize method, IColumnProvider.Initialize, IColumnProvider::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IColumnProvider interface, _win32_IColumnProvider_Initialize, shell.IColumnProvider_Initialize, shlobj/IColumnProvider::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IColumnProvider.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IColumnProvider::Initialize


## -description


Initializes an <a href="https://msdn.microsoft.com/06993217-2867-43f2-aa76-04b500bf8c17">IColumnProvider</a> interface.


## -parameters




### -param psci [in]

Type: <b>LPCSHCOLUMNINIT</b>

An <a href="https://msdn.microsoft.com/eebe47c8-b3ee-4316-b578-5404ed8f7920">SHCOLUMNINIT</a> structure with initialization information, including the folder whose contents are to be displayed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



