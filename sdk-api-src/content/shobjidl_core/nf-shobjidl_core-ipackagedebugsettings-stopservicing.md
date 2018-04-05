---
UID: NF:shobjidl_core.IPackageDebugSettings.StopServicing
title: IPackageDebugSettings::StopServicing method
author: windows-driver-content
description: Stops servicing the processes of the package if they are currently being serviced.
old-location: winrt\ipackagedebugsettings_stopservicing.htm
old-project: WinRT
ms.assetid: 91C20C41-8F20-4F9D-B22C-50D1D53FEB41
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], StopServicing method, IPackageDebugSettings::StopServicing, StopServicing method [Windows Runtime], StopServicing method [Windows Runtime], IPackageDebugSettings interface, StopServicing,IPackageDebugSettings.StopServicing, shobjidl_core/IPackageDebugSettings::StopServicing, winrt.ipackagedebugsettings_stopservicing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OVERLAPPED, *LPOVERLAPPED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IPackageDebugSettings.StopServicing
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IPackageDebugSettings::StopServicing method


## -description


Stops servicing the processes of the package if they are currently being serviced.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

