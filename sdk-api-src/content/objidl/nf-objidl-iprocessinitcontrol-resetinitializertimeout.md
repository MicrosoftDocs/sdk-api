---
UID: NF:objidl.IProcessInitControl.ResetInitializerTimeout
title: IProcessInitControl::ResetInitializerTimeout
author: windows-sdk-content
description: Sets the process initialization time-out.
old-location: com\iprocessinitcontrol_resetinitializertimeout.htm
tech.root: com
ms.assetid: 1045b9c9-d7ad-4306-bd9d-7c2a4bda9a62
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IProcessInitControl interface [COM],ResetInitializerTimeout method, IProcessInitControl.ResetInitializerTimeout, IProcessInitControl::ResetInitializerTimeout, ResetInitializerTimeout, ResetInitializerTimeout method [COM], ResetInitializerTimeout method [COM],IProcessInitControl interface, _com_iprocessinitcontrol_resetinitializertimeout, com.iprocessinitcontrol_resetinitializertimeout, objidlbase/IProcessInitControl::ResetInitializerTimeout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - IProcessInitControl.ResetInitializerTimeout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProcessInitControl::ResetInitializerTimeout


## -description


Sets the process initialization time-out.


## -parameters




### -param dwSecondsRemaining [in]

The number of seconds after this method is called before process initialization times out.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a>
 

 

