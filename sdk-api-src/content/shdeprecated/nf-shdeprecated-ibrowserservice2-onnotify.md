---
UID: NF:shdeprecated.IBrowserService2.OnNotify
title: IBrowserService2::OnNotify
author: windows-sdk-content
description: Deprecated. Calls the derived class from the base class on receipt of a WM_NOTIFY message. The derived class handles the message.
old-location: shell\IBrowserService2_OnNotify.htm
tech.root: shell
ms.assetid: 666d76da-0891-4645-8852-fc963be75369
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IBrowserService2 interface [Windows Shell],OnNotify method, IBrowserService2.OnNotify, IBrowserService2::OnNotify, OnNotify, OnNotify method [Windows Shell], OnNotify method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::OnNotify, shell.IBrowserService2_OnNotify, zone_IBrowserService2_OnNotify
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
 - IBrowserService2.OnNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::OnNotify


## -description


Deprecated. Calls the derived class from the base class on receipt of a <a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a> message. The derived class handles the message.


## -parameters




### -param pnm

TBD




#### - pcs [in, out]

Type: <b>tagNMHDR*</b>

A pointer to a <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that receives the initialization parameters passed to the window procedure (WinProc) of the class.


## -returns



Type: <b>LRESULT</b>

The return value specifies the result of the notification processing; it depends on the notification sent.



