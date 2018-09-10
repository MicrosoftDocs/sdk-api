---
UID: NF:shdeprecated.IBrowserService2.OnCreate
title: IBrowserService2::OnCreate
author: windows-sdk-content
description: Deprecated. Calls the derived class from the base class on receipt of a WM_CREATE message. The derived class handles the message.
old-location: shell\IBrowserService2_OnCreate.htm
tech.root: shell
ms.assetid: abfcb67a-c383-4480-9da9-788fb9cebf5e
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IBrowserService2 interface [Windows Shell],OnCreate method, IBrowserService2.OnCreate, IBrowserService2::OnCreate, OnCreate, OnCreate method [Windows Shell], OnCreate method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::OnCreate, shell.IBrowserService2_OnCreate, zone_IBrowserService2_OnCreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.OnCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::OnCreate


## -description


Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/en-us/library/ms632619(v=VS.85).aspx">WM_CREATE</a> message. The derived class handles the message.


## -parameters




### -param pcs [in]

Type: <b>tagCREATESTRUCTW*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms632603(v=VS.85).aspx">CREATESTRUCT</a> structure that receives the initialization parameters passed to the window procedure (WinProc) of the class.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



