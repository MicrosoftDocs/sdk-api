---
UID: NF:shobjidl.IBandHost.CreateBand
title: IBandHost::CreateBand
author: windows-sdk-content
description: Creates a specified band.
old-location: shell\IBandHost_CreateBand.htm
tech.root: Shell
ms.assetid: 7edf8d46-f925-4c4f-99b1-e792dce69222
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateBand, CreateBand method [Windows Shell], CreateBand method [Windows Shell],IBandHost interface, IBandHost interface [Windows Shell],CreateBand method, IBandHost.CreateBand, IBandHost::CreateBand, _shell_IBandHost_CreateBand, shell.IBandHost_CreateBand, shobjidl/IBandHost::CreateBand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IBandHost.CreateBand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



