---
UID: NF:shdeprecated.IBrowserService2.InitializeTravelLog
title: IBrowserService2::InitializeTravelLog method
author: windows-driver-content
description: Deprecated. Allows the derived class to specify a navigation record to be used in a new window.
old-location: shell\IBrowserService2_InitializeTravelLog.htm
old-project: shell
ms.assetid: ff2165da-e195-4cc1-ba89-c11eb37ac4c3
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IBrowserService2, IBrowserService2 interface [Windows Shell], InitializeTravelLog method, IBrowserService2::InitializeTravelLog, InitializeTravelLog method [Windows Shell], InitializeTravelLog method [Windows Shell], IBrowserService2 interface, InitializeTravelLog,IBrowserService2.InitializeTravelLog, shdeprecated/IBrowserService2::InitializeTravelLog, shell.IBrowserService2_InitializeTravelLog, zone_IBrowserService2_InitializeTravelLog
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
-	IBrowserService2.InitializeTravelLog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::InitializeTravelLog method


## -description


Deprecated. Allows the derived class to specify a navigation record to be used in a new window.


## -parameters




### -param ptl [in]

Type: <b><a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a>*</b>


          A pointer to an existing <a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a> object to be used for the new window.
        


### -param dw [in]

Type: <b>DWORD</b>


          The new browser window's ID.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



