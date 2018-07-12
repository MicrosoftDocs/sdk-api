---
UID: NF:shobjidl_core.ICreateProcessInputs.SetCreateFlags
title: ICreateProcessInputs::SetCreateFlags
author: windows-sdk-content
description: Set the flags that will be included in the call to CreateProcess.
old-location: shell\icreateprocessinputs_setcreateflags.htm
old-project: shell
ms.assetid: B929D77A-FEE4-40A1-8B40-34E2E73048F9
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetCreateFlags method, ICreateProcessInputs.SetCreateFlags, ICreateProcessInputs::SetCreateFlags, SetCreateFlags, SetCreateFlags method [Windows Shell], SetCreateFlags method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_setcreateflags, shobjidl_core/ICreateProcessInputs::SetCreateFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ICreateProcessInputs.SetCreateFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ICreateProcessInputs::SetCreateFlags


## -description


 Set the flags that will be included in the call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.


## -parameters




### -param dwCreationFlags [in]

The flags that will be passed to the <i>dwCreationFlags</i> parameter to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



 Any flags set by a previous call to <a href="https://msdn.microsoft.com/07D9E07E-BDF8-46F7-AB75-A3041E96F1A1">AddCreateFlags</a> or <b>SetCreateFlags </b> will be replaced by the values specified by <i>dwCreationFlags</i>. Use <b>AddCreateFlags</b> to set flags without clearing  flags that are already set.




## -see-also




<a href="https://msdn.microsoft.com/07D9E07E-BDF8-46F7-AB75-A3041E96F1A1">AddCreateFlags</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>



<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>
 

 

