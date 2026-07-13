---
UID: NF:objidl.IProcessInitControl.ResetInitializerTimeout
title: IProcessInitControl::ResetInitializerTimeout (objidl.h)
description: The IProcessInitControl::ResetInitializerTimeout method (objidl.h) sets the process initialization time-out. 
helpviewer_keywords: ["IProcessInitControl interface [COM]","ResetInitializerTimeout method","IProcessInitControl.ResetInitializerTimeout","IProcessInitControl::ResetInitializerTimeout","ResetInitializerTimeout","ResetInitializerTimeout method [COM]","ResetInitializerTimeout method [COM]","IProcessInitControl interface","_com_iprocessinitcontrol_resetinitializertimeout","com.iprocessinitcontrol_resetinitializertimeout","objidlbase/IProcessInitControl::ResetInitializerTimeout"]
old-location: com\iprocessinitcontrol_resetinitializertimeout.htm
tech.root: com
ms.assetid: 1045b9c9-d7ad-4306-bd9d-7c2a4bda9a62
ms.date: 08/12/2022
ms.keywords: IProcessInitControl interface [COM],ResetInitializerTimeout method, IProcessInitControl.ResetInitializerTimeout, IProcessInitControl::ResetInitializerTimeout, ResetInitializerTimeout, ResetInitializerTimeout method [COM], ResetInitializerTimeout method [COM],IProcessInitControl interface, _com_iprocessinitcontrol_resetinitializertimeout, com.iprocessinitcontrol_resetinitializertimeout, objidlbase/IProcessInitControl::ResetInitializerTimeout
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProcessInitControl::ResetInitializerTimeout
 - objidl/IProcessInitControl::ResetInitializerTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IProcessInitControl.ResetInitializerTimeout
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

<a href="/windows/desktop/api/objidl/nn-objidl-iprocessinitcontrol">IProcessInitControl</a>
