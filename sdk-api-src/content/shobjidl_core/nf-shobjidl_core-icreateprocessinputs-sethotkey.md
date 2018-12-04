---
UID: NF:shobjidl_core.ICreateProcessInputs.SetHotKey
title: ICreateProcessInputs::SetHotKey
author: windows-sdk-content
description: Sets the hot key for the application.
old-location: shell\icreateprocessinputs_sethotkey.htm
tech.root: shell
ms.assetid: B54934CA-6345-4B06-BA5F-75FA4B5CEE4F
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetHotKey method, ICreateProcessInputs.SetHotKey, ICreateProcessInputs::SetHotKey, SetHotKey, SetHotKey method [Windows Shell], SetHotKey method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_sethotkey, shobjidl_core/ICreateProcessInputs::SetHotKey
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICreateProcessInputs.SetHotKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateProcessInputs::SetHotKey


## -description


Sets the hot key for the application.


## -parameters




### -param wHotKey [in]

The hotkey to assign to the application. See the documentation of the <b>hStdIn</b> member of the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure for more information.


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



 This method also sets the <b>STARTF_USEHOTKEY</b> flag in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>



<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>
 

 

