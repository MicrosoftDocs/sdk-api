---
UID: NF:shlobj.IColumnProvider.Initialize
title: IColumnProvider::Initialize (shlobj.h)
description: Initializes an IColumnProvider interface.
helpviewer_keywords: ["IColumnProvider interface [Windows Shell]","Initialize method","IColumnProvider.Initialize","IColumnProvider::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IColumnProvider interface","_win32_IColumnProvider_Initialize","shell.IColumnProvider_Initialize","shlobj/IColumnProvider::Initialize"]
old-location: shell\IColumnProvider_Initialize.htm
tech.root: shell
ms.assetid: 4975042d-549e-4032-9f42-468dc7e3c20e
ms.date: 12/05/2018
ms.keywords: IColumnProvider interface [Windows Shell],Initialize method, IColumnProvider.Initialize, IColumnProvider::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IColumnProvider interface, _win32_IColumnProvider_Initialize, shell.IColumnProvider_Initialize, shlobj/IColumnProvider::Initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IColumnProvider::Initialize
 - shlobj/IColumnProvider::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IColumnProvider.Initialize
---

# IColumnProvider::Initialize


## -description

Initializes an <a href="/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider">IColumnProvider</a> interface.

## -parameters

### -param psci [in]

Type: <b>LPCSHCOLUMNINIT</b>

An <a href="/windows/desktop/api/shlobj/ns-shlobj-shcolumninit">SHCOLUMNINIT</a> structure with initialization information, including the folder whose contents are to be displayed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.