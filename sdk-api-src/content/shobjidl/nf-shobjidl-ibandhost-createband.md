---
UID: NF:shobjidl.IBandHost.CreateBand
title: IBandHost::CreateBand (shobjidl.h)
description: Creates a specified band.
helpviewer_keywords: ["CreateBand","CreateBand method [Windows Shell]","CreateBand method [Windows Shell]","IBandHost interface","IBandHost interface [Windows Shell]","CreateBand method","IBandHost.CreateBand","IBandHost::CreateBand","_shell_IBandHost_CreateBand","shell.IBandHost_CreateBand","shobjidl/IBandHost::CreateBand"]
old-location: shell\IBandHost_CreateBand.htm
tech.root: shell
ms.assetid: 7edf8d46-f925-4c4f-99b1-e792dce69222
ms.date: 12/05/2018
ms.keywords: CreateBand, CreateBand method [Windows Shell], CreateBand method [Windows Shell],IBandHost interface, IBandHost interface [Windows Shell],CreateBand method, IBandHost.CreateBand, IBandHost::CreateBand, _shell_IBandHost_CreateBand, shell.IBandHost_CreateBand, shobjidl/IBandHost::CreateBand
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IBandHost::CreateBand
 - shobjidl/IBandHost::CreateBand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IBandHost.CreateBand
---

# IBandHost::CreateBand


## -description

Creates a specified band.

## -parameters

### -param rclsidBand [in]

Type: <b>REFCLSID</b>

A reference to a CLSID. Used to ensure a duplicate band is not created.

### -param fAvailable [in]

Type: <b>BOOL</b>

Specifies band availability.

### -param fVisible [in]

Type: <b>BOOL</b>

Specifies band visibility.

### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired IID.

### -param ppv [out]

Type: <b>void**</b>

Contains the address of a pointer to a band specified by <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

