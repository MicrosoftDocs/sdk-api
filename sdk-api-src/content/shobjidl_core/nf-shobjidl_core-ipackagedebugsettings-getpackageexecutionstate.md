---
UID: NF:shobjidl_core.IPackageDebugSettings.GetPackageExecutionState
title: IPackageDebugSettings::GetPackageExecutionState method
author: windows-driver-content
description: Gets the execution state for the processes of the specified package.
old-location: winrt\ipackagedebugsettings_getpackageexecutionstate.htm
old-project: WinRT
ms.assetid: 0D3FD95D-C958-4388-90F4-03DE2F75DF64
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetPackageExecutionState method [Windows Runtime], GetPackageExecutionState method [Windows Runtime], IPackageDebugSettings interface, GetPackageExecutionState,IPackageDebugSettings.GetPackageExecutionState, IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], GetPackageExecutionState method, IPackageDebugSettings::GetPackageExecutionState, PES_RUNNING, PES_SUSPENDED, PES_SUSPENDING, PES_TERMINATED, PES_UNKNOWN, shobjidl_core/IPackageDebugSettings::GetPackageExecutionState, winrt.ipackagedebugsettings_getpackageexecutionstate
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
-	IPackageDebugSettings.GetPackageExecutionState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IPackageDebugSettings::GetPackageExecutionState method


## -description


Gets the execution state for the processes of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


### -param packageExecutionState [out]

Type: <b><a href="https://msdn.microsoft.com/8BE433AC-34E6-42D7-9F8B-63AECAC96996">PACKAGE_EXECUTION_STATE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/8BE433AC-34E6-42D7-9F8B-63AECAC96996">PACKAGE_EXECUTION_STATE</a>-typed value that indicates the execution state. Here are possible values:



#### PES_UNKNOWN (0)



#### PES_RUNNING (1)



#### PES_SUSPENDING (2)



#### PES_SUSPENDED (3)



#### PES_TERMINATED (4)


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

