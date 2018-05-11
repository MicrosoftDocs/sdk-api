---
UID: NF:shdeprecated.IBrowserService2.Offline
title: IBrowserService2::Offline
author: windows-driver-content
description: Deprecated. Checks for and updates the browser's offline status, synchronzing the state between the base class and any derived classes.
old-location: shell\IBrowserService2_Offline.htm
old-project: shell
ms.assetid: c1f4a4bd-2fd8-424f-b84a-d68b7e2e019c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IBrowserService2 interface [Windows Shell],Offline method, IBrowserService2.Offline, IBrowserService2::Offline, Offline, Offline method [Windows Shell], Offline method [Windows Shell],IBrowserService2 interface, SBSC_QUERY, SBSC_TOGGLE, shdeprecated/IBrowserService2::Offline, shell.IBrowserService2_Offline, zone_IBrowserService2_Offline
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
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService2.Offline
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::Offline


## -description


Deprecated. Checks for and updates the browser's offline status, synchronzing the state between the base class and any derived classes.


## -parameters




### -param iCmd [in]

Type: <b>int</b>

One of the following commands.



#### SBSC_QUERY

Queries the offline state. The method's return value contains the answer.



#### SBSC_TOGGLE

Toggles the offline state.


## -returns



Type: <b>HRESULT</b>

In the case of SBSC_TOGGLE, returns standard error codes. In the case of SBSC_QUERY, returns S_OK if offline, S_FALSE otherwise.



