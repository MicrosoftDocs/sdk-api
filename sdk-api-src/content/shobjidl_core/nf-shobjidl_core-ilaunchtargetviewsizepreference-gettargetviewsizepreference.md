---
UID: NF:shobjidl_core.ILaunchTargetViewSizePreference.GetTargetViewSizePreference
title: ILaunchTargetViewSizePreference::GetTargetViewSizePreference
author: windows-sdk-content
description: Retrieves the preferred view size of the application being launched.
old-location: shell\ILaunchTargetViewSizePreference_GetTargetViewSizePreference.htm
tech.root: shell
ms.assetid: 2C852FD1-09FD-45B6-A493-07DEE72BEA4C
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetTargetViewSizePreference, GetTargetViewSizePreference method [Windows Shell], GetTargetViewSizePreference method [Windows Shell],ILaunchTargetViewSizePreference interface, ILaunchTargetViewSizePreference interface [Windows Shell],GetTargetViewSizePreference method, ILaunchTargetViewSizePreference.GetTargetViewSizePreference, ILaunchTargetViewSizePreference::GetTargetViewSizePreference, shell.ILaunchTargetViewSizePreference_GetTargetViewSizePreference, shobjidl_core/ILaunchTargetViewSizePreference::GetTargetViewSizePreference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - shobjidl_core.h
api_name:
 - ILaunchTargetViewSizePreference.GetTargetViewSizePreference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILaunchTargetViewSizePreference::GetTargetViewSizePreference


## -description


Retrieves the preferred view size of the application being launched.


## -parameters




### -param targetSizeOnLaunch [out]

Type: <b><a href="https://msdn.microsoft.com/20B27858-D5BC-4800-AE3F-C01A017ABBF7">APPLICATION_VIEW_SIZE_PREFERENCE</a>*</b>

Contains the address of a pointer to an <a href="https://msdn.microsoft.com/20B27858-D5BC-4800-AE3F-C01A017ABBF7">APPLICATION_VIEW_SIZE_PREFERENCE</a>  for the target application.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3535E9EF-265E-4278-8E0D-60AA8A34C316">ILaunchTargetViewSizePreference</a>
 

 

